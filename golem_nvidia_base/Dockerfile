FROM ubuntu:jammy-20231004

ARG DEBIAN_FRONTEND=noninteractive

COPY config-virt /usr/src/config-virt

RUN apt-get update && apt-get install -y \
	wget \
	kmod \
	xz-utils \
	pkg-config \
	&& rm -rf /var/lib/apt/lists/*

RUN cd /usr/src \
	&& cd /usr/src \
	&& wget https://download.nvidia.com/XFree86/Linux-x86_64/570.86.16/NVIDIA-Linux-x86_64-570.86.16.run \
	&& chmod +x NVIDIA-Linux-x86_64-570.86.16.run \
	&& ./NVIDIA-Linux-x86_64-570.86.16.run -s --no-kernel-modules \
	&& rm -rf /usr/src/*
	
