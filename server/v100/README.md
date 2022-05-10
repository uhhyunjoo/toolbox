# Install Pytorch
[wiki/CUDA](https://en.wikipedia.org/wiki/CUDA)
> CUDA SDK 10.0 – 10.2 support for compute capability 3.0 – 7.5 (Kepler, Maxwell, Pascal, Volta, Turing). Last version with support for compute capability 3.x (Kepler). 10.2 is the last official release for macOS, as support will not be available for macOS in newer releases.

[pytorch/versions](https://pytorch.org/get-started/previous-versions/)
```
# CUDA 10.1
pip install torch==1.8.1+cu101 torchvision==0.9.1+cu101 torchaudio==0.8.1 -f https://download.pytorch.org/whl/torch_stable.html
```

cuda / pytorch version 이 맞는 명령어로 install

## CUDA version

```
nvcc: NVIDIA (R) Cuda compiler driver
Copyright (c) 2005-2017 NVIDIA Corporation
Built on Fri_Nov__3_21:07:56_CDT_2017
Cuda compilation tools, release 9.1, V9.1.85
```

```
Tue May 10 16:03:20 2022       
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 410.104      Driver Version: 410.104      CUDA Version: 10.0     |
|-------------------------------+----------------------+----------------------+
| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|===============================+======================+======================|
|   0  Tesla V100-SXM2...  On   | 00000000:06:00.0 Off |                    0 |
| N/A   73C    P0   286W / 300W |  26742MiB / 32480MiB |     96%      Default |
+-------------------------------+----------------------+----------------------+
|   1  Tesla V100-SXM2...  On   | 00000000:07:00.0 Off |                    0 |
| N/A   57C    P0    99W / 300W |  26478MiB / 32480MiB |     28%      Default |
+-------------------------------+----------------------+----------------------+
|   2  Tesla V100-SXM2...  On   | 00000000:0A:00.0 Off |                    0 |
| N/A   52C    P0   122W / 300W |  24926MiB / 32480MiB |     24%      Default |
+-------------------------------+----------------------+----------------------+
|   3  Tesla V100-SXM2...  On   | 00000000:0B:00.0 Off |                    0 |
| N/A   48C    P0   124W / 300W |  24926MiB / 32480MiB |     12%      Default |
+-------------------------------+----------------------+----------------------+
|   4  Tesla V100-SXM2...  On   | 00000000:85:00.0 Off |                    0 |
| N/A   48C    P0   127W / 300W |  24926MiB / 32480MiB |     22%      Default |
+-------------------------------+----------------------+----------------------+
|   5  Tesla V100-SXM2...  On   | 00000000:86:00.0 Off |                    0 |
| N/A   50C    P0    74W / 300W |  24926MiB / 32480MiB |      0%      Default |
+-------------------------------+----------------------+----------------------+
|   6  Tesla V100-SXM2...  On   | 00000000:89:00.0 Off |                    0 |
| N/A   47C    P0    77W / 300W |  24926MiB / 32480MiB |     17%      Default |
+-------------------------------+----------------------+----------------------+
|   7  Tesla V100-SXM2...  On   | 00000000:8A:00.0 Off |                    0 |
| N/A   40C    P0    44W / 300W |      0MiB / 32480MiB |      0%      Default |
+-------------------------------+----------------------+----------------------+
                                                                               
+-----------------------------------------------------------------------------+
| Processes:                                                       GPU Memory |
|  GPU       PID   Type   Process name                             Usage      |
|=============================================================================|
|    0     51918      C   cdva                                       26729MiB |
|    1     56785      C   python                                     26465MiB |
|    2     56785      C   python                                     24913MiB |
|    3     56785      C   python                                     24913MiB |
|    4     56785      C   python                                     24913MiB |
|    5     56785      C   python                                     24913MiB |
|    6     56785      C   python                                     24913MiB |
+-----------------------------------------------------------------------------+
```

## Environment
```
Collecting environment information...
PyTorch version: N/A
Is debug build: N/A
CUDA used to build PyTorch: N/A
ROCM used to build PyTorch: N/A

OS: Ubuntu 18.04.2 LTS (x86_64)
GCC version: (Ubuntu 4.9.3-13ubuntu2) 4.9.3
Clang version: Could not collect
CMake version: version 3.10.2
Libc version: glibc-2.15

Python version: 2.7.17 (default, Apr 15 2020, 17:20:14)  [GCC 7.5.0] (64-bit runtime)
Python platform: Linux-4.15.0-39-generic-x86_64-with-Ubuntu-18.04-bionic
Is CUDA available: N/A
CUDA runtime version: 9.1.85
GPU models and configuration: 
GPU 0: Tesla V100-SXM2-32GB
GPU 1: Tesla V100-SXM2-32GB
GPU 2: Tesla V100-SXM2-32GB
GPU 3: Tesla V100-SXM2-32GB
GPU 4: Tesla V100-SXM2-32GB
GPU 5: Tesla V100-SXM2-32GB
GPU 6: Tesla V100-SXM2-32GB
GPU 7: Tesla V100-SXM2-32GB

Nvidia driver version: 410.104
cuDNN version: Could not collect
HIP runtime version: N/A
MIOpen runtime version: N/A
Is XNNPACK available: N/A

Versions of relevant libraries:
[pip] numpy==1.13.3
[conda] Could not collect
```
