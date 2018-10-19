FROM nvidia/cuda:9.0-cudnn7-devel-ubuntu16.04

RUN apt-get update && apt-get install -y wget zlib1g-dev libssl-dev curl git
RUN wget https://www.python.org/ftp/python/3.6.3/Python-3.6.3.tgz && tar -xvf Python-3.6.3.tgz
RUN cd Python-3.6.3 && ./configure && make && make install

RUN pip3 install --upgrade pip
RUN pip3 install --no-cache-dir torchvision tensorflow-gpu numpy pyyaml mkl mkl-include setuptools cmake cffi typing

RUN ln -fs /usr/local/bin/python3 /usr/local/bin/python && rm Python-3.6.3.tgz && rm -R Python-3.6.3

RUN cd /home && git clone --recursive https://github.com/pytorch/pytorch && cd pytorch && python setup.py install

ENV LANG C.UTF-8
