IMAGE_NAME = ERC_IMAGE
PYTHON_VERSION = 3.6

UID:=$(shell id -u)
USER_NAME:=$(shell whoami)
POS_GPUS=all
PASSWORD=0000

UBUNTU_VERSION=20.04
CUDA_VERSION=10.2
CUDNN_VERSION=8
CONDA_ENV_NAME=torch

IMAGE_TAG= cuda10.2 # cuda$(CUDA_VERSION)-cudnn$(CUDNN_VERSION)-devel-ubuntu$(UBUNTU_VERSION)
CONTAINER_NAME=ser

#### Should change to unused ports ###
TBP=8883
JNBP=8884

docker-base:
	$(eval IMAGE_NAME := $(IMAGE_NAME):$(IMAGE_TAG))
	@nvidia-docker build -t hjlee/$(IMAGE_NAME) \
    --build-arg UID=$(UID) \
    --build-arg USER_NAME=$(USER_NAME) \
    --build-arg UBUNTU_VERSION=$(UBUNTU_VERSION) \
    --build-arg CUDA_VERSION=$(CUDA_VERSION) \
    --build-arg CUDNN_VERSION=$(CUDNN_VERSION) \
    --build-arg PYTHON_VERSION=$(PYTHON_VERSION) \
    --build-arg CONDA_ENV_NAME=$(CONDA_ENV_NAME) \
    -f Dockerfile \
    .

docker-run:
	$(eval IMAGE_NAME := $(IMAGE_NAME):$(IMAGE_TAG))
	@nvidia-docker run -it -u ${USER_NAME} \
		--name ${USER_NAME}_${CONTAINER_NAME} \
		-p ${TBP}:6006 \
		-p ${JNBP}:8888 \
		-e "TERM=xterm-256color" \
		-w /home/${USER_NAME}/workspace \
		-v /home/${USER_NAME}/workspace:/home/${USER_NAME}/workspace \
		-v /data1:/data1: \
		-v /data2:/data2: \
		-v /data3:/data3: \
		-v /data4:/data4: \
		-v /data5:/data5: \
		-v /data6:/data6: \
		-e NVIDIA_VISIBLE_DEVICES=${POS_GPUS} \
		--shm-size=32G \
		${USER_NAME}/${IMAGE_NAME} \
		/bin/bash