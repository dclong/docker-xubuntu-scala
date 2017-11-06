# Xubuntu with Scala in Docker

## Detailed Information

OS: Ubuntu 16.04

Desktop Environment: Xfce

Remote Desktop: NoMachine

Additional Software: Firefox, OpenJDK 8, Scala 2.11

## About the Author

[Personal Blog](http://www.legendu.net)   |   [GitHub](https://github.com/dclong)   |   [Bitbucket](https://bitbucket.org/dclong/)   |   [LinkedIn](http://www.linkedin.com/in/ben-chuanlong-du-1239b221/)



## How to run

### Build

```
./build.sh
```

### Docker pull command

```
docker pull dclong/xubuntu-scala
```

### Usage

```
docker run -d -p 4000:4000 \
    -e DOCKER_USER_ID=`id -u` \
    -e DOCKER_USER=`id -un` \
    -e DOCKER_PASSWORD=`id -un` \
    -v $HOME:/`id -un` \
    --cap-add=SYS_PTRACE \
    dclong/xubuntu-scala
```

```
docker run -d -p 4000:4000 
    -e DOCKER_USER_ID=`id -u` 
    -e DOCKER_USER=`id -un` 
    -v $HOME/dropbox:/home/`id -un`/Dropbox 
    --cap-add=SYS_PTRACE 
    dclong/xubuntu-scala
```

A default user `dclong` with password `dclong` is used if not specified when running the docker image.

### Connect to the container

Download the NoMachine client from <https://www.nomachine.com/download>, 
install the client, 
create a new connection to your public ip, port 4000, NX protocol, 
use a user on the host OS and the corresponding password for authentication. 
