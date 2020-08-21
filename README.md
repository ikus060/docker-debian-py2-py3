# docker-debian-py2-py3

**DEPRECATED:** in favour of https://github.com/ikus060/docker-python

This repository contains a Dockerfile to create a docker container with
Python2.7 and corresponding Python3 installed from the OS packages.

This Dockerfile has been published as a trusted build to the public Docker Registry.

## Supported tags
* jessie
* wheezy
* stretch

## What is docker-debian-py2-py3?
This image is intended to be used as part of a CICD build system like Gitlab to
help you compile your python projects in a controlled environment. Compared to
`python` images, these images install python using the OS packages
instead of using a tar.gz.

By [IKUS Software inc](https://www.ikus-soft.com)
