FROM buildpack-deps:jessie

RUN apt-get update && apt-get install -y --no-install-recommends \
                python python-dev python-pip python-setuptools python3 python3-dev python3-pip python3-setuptools \
    && pip2 install pip setuptools tox nose coverage wheel twine --upgrade \
    && pip3 install pip setuptools tox nose coverage wheel twine --upgrade \
    && rm -rf /var/lib/apt/lists/*

# Needed. Otherwise break python3 encoding.
# see https://bugs.python.org/issue19846
ENV LANG=C.UTF-8
