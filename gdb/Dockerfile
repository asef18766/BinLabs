FROM ubuntu:22.04
ENV DEBIAN_FRONTEND noninteractive
RUN apt update && apt install -y gdbserver qemu-system-arm wget
RUN wget https://github.com/pwndbg/pwndbg/releases/download/2025.04.18/pwndbg_2025.04.18_amd64.deb && \
    dpkg -i pwndbg_2025.04.18_amd64.deb && \
    rm pwndbg_2025.04.18_amd64.deb
RUN apt install -y gdb-multiarch

# libdebug, not very necessary, but it's good for native debugging script
# RUN apt install -y python3 python3-dev g++ libdwarf-dev libelf-dev libiberty-dev linux-headers-generic libc6-dbg

# pwntools
RUN apt-get install -y python3 python3-pip python3-dev git libssl-dev libffi-dev build-essential
RUN python3 -m pip install --upgrade pwntools

# only for cggc challenges, not necessary in all situation
RUN apt install iproute2
