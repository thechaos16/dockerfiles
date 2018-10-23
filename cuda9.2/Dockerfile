FROM nvidia/cuda:9.2-cudnn7-devel-ubuntu16.04

RUN apt-get update && apt-get install -y wget zlib1g-dev libssl-dev curl
RUN wget https://www.python.org/ftp/python/3.6.3/Python-3.6.3.tgz && tar -xvf Python-3.6.3.tgz
RUN cd Python-3.6.3 && ./configure && make && make install

RUN pip3 install --upgrade pip && pip install --no-cache-dir torchvision && pip install --no-cache-dir torch_nightly -f https://download.pytorch.org/whl/nightly/cu92/torch_nightly.html

RUN ln -fs /usr/local/bin/python3 /usr/local/bin/python && rm Python-3.6.3.tgz && rm -R Python-3.6.3

ENV LANG C.UTF-8
