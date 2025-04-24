FROM node:bullseye-slim
ENV DEBIAN_FRONTEND noninteractive
RUN apt update && apt install -y python3 python3-pip libpython3-dev
RUN pip install --upgrade frida-tools frida
#RUN npm install -g frida tsc