# uzyexe/packer [![Circle CI](https://circleci.com/gh/uzyexe/dockerfile-packer.svg?style=svg)](https://circleci.com/gh/uzyexe/dockerfile-packer)

## What is packer

Packer is a tool for creating machine and container images for multiple platforms from a single source configuration.

[https://www.packer.io/](https://www.packer.io/)

## Dockerfile

[**Trusted Build**](https://hub.docker.com/r/uzyexe/packer/)

This Docker image is based on the official [alpine:3.3](https://hub.docker.com/_/alpine/) base image.

## How to use this image

```
usage: docker run -v /data:/data uzyexe/packer [--version] [--help] <command> [<args>]

Available commands are:
    build       build image(s) from template
    fix         fixes templates from old versions of packer
    inspect     see components of a template
    push        push a template and supporting files to a Packer build service
    validate    check that a template is valid
    version     Prints the Packer version
```

## Using

**Please note: Create by your Packer templates files (.json) is `/data` directory**

### packer build

```
docker run --rm -v /data:/data uzyexe/packer build [options]
```

### packer fix

```
docker run --rm -v /data:/data uzyexe/packer fix [options] TEMPLATE
```

### packer inspect

```
docker run --rm -v /data:/data uzyexe/packer inspect TEMPLATE
```

### packer push

```
docker run --rm -v /data:/data uzyexe/packer push [options] TEMPLATE
```

### packer validate

```
docker run --rm -v /data:/data uzyexe/packer validate [options] TEMPLATE
```

### packer version

```
docker run --rm uzyexe/packer version
```
