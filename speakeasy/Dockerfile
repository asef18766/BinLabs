FROM ubuntu:22.04
ENV DEBIAN_FRONTEND noninteractive
RUN apt update && apt install -y python3 python3-pip libpython3-dev git
RUN pip3 install git+https://github.com/mandiant/speakeasy.git