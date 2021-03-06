# dfir
Collection of the most popular and widely used open-source forensic tools in a lightweight and fast docker image.

## Overview
Focus what on what matters the most! Memory (volatility), registry (regripper), filesystem (sleuthkit). 

Volatility comes with SANS plugins to help you speed up your investigations.

The Docker image is based on [Alpine Linux](https://hub.docker.com/_/alpine/), the most lightweight linux container distribution.
Some of the tool are provided by the great folks of [SANS](https://github.com/sans-dfir). 

### Install Docker
Wait! It's dangerous to go alone! 

Make sure you have the Docker engine installed. Click [here](https://docs.docker.com/install/) for detailed installation instructions.
Build the image with one of the following ways :

### Build from Docker registry (Recommended)
Just :
```
sudo docker pull nov3mb3r/dfir
```
Simple isn't it?

### Run 
To run created image :
```
sudo docker run -it nov3mb3r/dfir /bin/ash
```
Access your case files with a shared folder between your working directory and the container.

##### Preserve the authenticity of your evidence: Make sure you don't tamper with the data, by granting read only permissions to the container. 
```
$ sudo docker run -it -v ~/cases:/cases:ro nov3mb3r/dfir /bin/ash 
```
