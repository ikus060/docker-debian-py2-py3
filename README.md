# docker-debian-py2-py3
This repository contains a Dockerfile to create a docker container with Python 2.7 and corresponding python 3 installed from the OS packages.

This Dockerfile has been published as a trusted build to the public Docker Registry.

## Supported tags
* jessie
* wheezy
* stretch

## What is docker-debian-py2-py3?
This image is intended to be used as part of a CICD build system like Jenkins to help you compile your python projects in a controlled environment. Compared to `python` images, these images install python using the OS packages instead of using a tar.gz.

## How to use in Jenkinsfile?
```
node {
    checkout scm
    
    docker.image("ikus060/docker-debian-py2-py3:jessie").inside {
        stage ('Initialize') {
            sh 'pip install pip setuptools nose --upgrade'
        }
        stage ('Build') {
            sh 'python setup.py nosetests --with-xunit'
        }
        stage ('Post') {
            junit 'nosetest*.xml'
        }
    }
}
```

By [Patrik Dufresne Service Logiciel inc.](http://www.patrikdufresne.com)
