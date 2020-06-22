FROM ubuntu:19.10
LABEL maintainer="Abhishek N. Kulkarni <ankulkarni@wpi.edu>"

# Set clock and timezone for docker image
RUN echo 'Etc/UTC' > /etc/timezone && \
    ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime && \
    apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*

# Package installation, setup, vcs, build utilities
RUN apt update && \
	RUNLEVEL=1 DEBIAN_FRONTEND=noninteractive && \
	apt-get install -y software-properties-common wget nano 
	
RUN apt update && \
	RUNLEVEL=1 DEBIAN_FRONTEND=noninteractive && \
	apt-get install -y python 