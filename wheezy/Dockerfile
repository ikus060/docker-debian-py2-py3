FROM buildpack-deps:wheezy-scm

RUN apt-get update && apt-get install -y --no-install-recommends \
                python python-dev python-pip python3 python3-dev python3-pip \
	&& rm -rf /var/lib/apt/lists/*

# Needed. Otherwise break python3 encoding.
# see https://bugs.python.org/issue19846
ENV LANG=C.UTF-8
