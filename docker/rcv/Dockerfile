ARG UBUNTU_VERSION=18.04
ARG CUDA_VERSION=10.2
ARG CUDNN_VERSION=8

FROM nvidia/cuda:${CUDA_VERSION}-cudnn${CUDNN_VERSION}-devel-ubuntu${UBUNTU_VERSION}
LABEL maintainer "https://uhhyunjoo.dev/"

ARG CUDA_VERSION
ARG UID=
ARG USER_NAME=
ARG PYTHON_VERSION=
ARG CONDA_ENV_NAME=

# Let us install tzdata painlessly
ENV DEBIAN_FRONTEND=noninteractive

# Needed for string substitution
SHELL ["/bin/bash", "-c"]

# https://forums.developer.nvidia.com/t/18-04-cuda-docker-image-is-broken/212892/9
RUN rm /etc/apt/sources.list.d/cuda.list
RUN rm /etc/apt/sources.list.d/nvidia-ml.list

RUN apt-get update && apt-get install -y --no-install-recommends \
    apt-utils \
    build-essential \
    ca-certificates \
    tmux \
    ccache \
    cmake \
    curl \
    git \
    libfreetype6-dev \
    libhdf5-serial-dev \
    libzmq3-dev \
    libjpeg-dev \
    libpng-dev \
    libsm6 \
    libxext6 \
    libxrender-dev \
    pkg-config \
    software-properties-common \
    ssh \
    sudo \
    unzip \
    vim \
    wget
RUN rm -rf /var/lib/apt/lists/*

# See http://bugs.python.org/issue19846
ENV LANG C.UTF-8
RUN curl -o /tmp/miniconda.sh -sSL http://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh && \
    chmod +x /tmp/miniconda.sh && \
    bash /tmp/miniconda.sh -bfp /usr/local && \
    rm /tmp/miniconda.sh
RUN conda update -y conda

# Create a user
RUN adduser $USER_NAME -u $UID --quiet --gecos "" --disabled-password && \
    echo "$USER_NAME ALL=(root) NOPASSWD:ALL" > /etc/sudoers.d/$USER_NAME && \
    chmod 0440 /etc/sudoers.d/$USER_NAME

# For connecting via ssh
RUN echo "PasswordAuthentication yes" >> /etc/ssh/sshd_config && \
    echo "PermitEmptyPasswords yes" >> /etc/ssh/sshd_config && \
    echo "UsePAM no" >> /etc/ssh/sshd_config

USER $USER_NAME
SHELL ["/bin/bash", "-c"]

# Create the conda environment
RUN conda create -n $CONDA_ENV_NAME python=$PYTHON_VERSION
ENV PATH /usr/local/envs/$CONDA_ENV_NAME/bin:$PATH
RUN echo "source activate ${CONDA_ENV_NAME}" >> ~/.bashrc

# Enable jupyter lab
RUN source activate ${CONDA_ENV_NAME} && \
    conda install -c conda-forge jupyterlab && \
    jupyter serverextension enable --py jupyterlab --sys-prefix

# Install the packages
RUN source activate ${CONDA_ENV_NAME} && \
    conda install pytorch torchvision torchaudio cudatoolkit=${CUDA_VERSION} -c pytorch

# Reference
# https://github.com/pytorch/pytorch/blob/master/Dockerfile
# https://gist.github.com/GzuPark/b89344cb93320e395ec357bc711a8799