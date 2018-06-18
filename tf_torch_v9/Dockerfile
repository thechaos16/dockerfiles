FROM nvidia/cuda:9.0-cudnn7-devel-ubuntu16.04

RUN apt-get update && apt-get install -y wget zlib1g-dev libssl-dev curl
RUN wget https://www.python.org/ftp/python/3.6.3/Python-3.6.3.tgz && tar -xvf Python-3.6.3.tgz
RUN cd Python-3.6.3 && ./configure && make && make install

RUN pip3 install --upgrade pip
RUN pip3 install --no-cache-dir http://download.pytorch.org/whl/cu90/torch-0.4.0-cp36-cp36m-linux_x86_64.whl && pip install --no-cache-dir torchvision tensorflow-gpu

RUN ln -fs /usr/local/bin/python3 /usr/local/bin/python && rm Python-3.6.3.tgz && rm -R Python-3.6.3

ENV LANG C.UTF-8
