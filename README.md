# Docker Alpine glibc

[![Docker Stars](https://img.shields.io/docker/stars/gitbook/alpine-glibc.svg?style=flat-square)](https://hub.docker.com/r/gitbook/alpine-glibc/)
[![Docker Pulls](https://img.shields.io/docker/pulls/gitbook/alpine-glibc.svg?style=flat-square)](https://hub.docker.com/r/gitbook/alpine-glibc/)
[![](https://badge.imagelayers.io/gitbook/alpine-glibc:latest.svg)](https://imagelayers.io/?images=gitbook/alpine-glibc:latest)

This image is based on Alpine Linux image, which is only a 5MB image, and contains `glibc` to enable
proprietary projects compiled against `glibc` (e.g. OracleJDK, Anaconda) work on Alpine. It has the added of benefit of being correctly versioned with **semver** (unlike most docker images).

This image includes some quirks to make `glibc` work side by side with `musl` `libc` (default in Apline).

### Usage Example

This image is intended to be a base image for your projects, so you may use it like this:

```Dockerfile
FROM gitbook/alpine-glibc

COPY ./my_app /usr/local/bin/my_app
```

```sh
$ docker build -t my_app .
```

### Thanks

Original code inspired from: [frol/docker-alpine-glibc](https://github.com/frol/docker-alpine-glibc)
