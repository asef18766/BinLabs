FROM node:bookworm-slim
ENV DEBIAN_FRONTEND noninteractive
RUN apt update && apt install -y python3 python3-pip libpython3-dev wget
RUN apt install -y pipx && pipx install frida-tools
RUN wget https://github.com/frida/frida/releases/download/16.7.14/frida-server-16.7.14-linux-x86_64.xz && \
    xz -d frida-server-16.7.14-linux-x86_64.xz && \
    mv frida-server-16.7.14-linux-x86_64 /bin/frida-server && \
    chmod +x /bin/frida-server
#RUN npm install -g frida tsc