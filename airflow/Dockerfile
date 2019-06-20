FROM ubuntu:18.04

RUN apt-get update && apt-get install -y python3.6-dev python3-pip libsasl2-modules libsasl2-dev vim git screen
RUN pip3 install --no-cache-dir sasl thrift thrift_sasl pyhive pandas numpy apache-airflow tqdm
RUN airflow initdb

WORKDIR /root/airflow
EXPOSE 8080
CMD /bin/bash
