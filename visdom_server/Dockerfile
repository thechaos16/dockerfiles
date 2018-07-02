FROM jegadroid/visdom

RUN apt-get update; apt-get install -y git
RUN git clone https://github.com/facebookresearch/visdom.git
RUN cd visdom; pip install -e .
