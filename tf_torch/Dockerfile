FROM tensorflow/tensorflow:latest-gpu-py3

RUN apt-get -y update && echo "export PATH=/usr/local/bin:/usr/local/nvidia/bin:/usr/local/cuda/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin">> /etc/profile
RUN echo "export CUDA_VERSION=8.0">> /etc/profile
RUN echo "export CUDA_PKG_VERSION=8-0=8.0.44-1">> /etc/profile
RUN echo "export LD_LIBRARY_PATH=/usr/local/nvidia/lib:/usr/local/nvidia/lib64">> /etc/profile
RUN echo "export LIBRARY_PATH=/usr/local/cuda/lib64/stubs">> /etc/profile
RUN echo "export LANG=C.UTF-8">> /etc/profile

RUN pip install --no-cache-dir keras
RUN pip install --no-cache-dir http://download.pytorch.org/whl/cu80/torch-0.3.0.post4-cp35-cp35m-linux_x86_64.whl
RUN pip install --no-cache-dir torchvision
