FROM buildpack-deps:stretch

RUN apt-get update && apt-get install -y --no-install-recommends \
                python python-dev python-pip python-setuptools python3 python3-dev python3-pip python3-setuptools \
	&& rm -rf /var/lib/apt/lists/*

# Needed. Otherwise break python3 encoding.
# see https://bugs.python.org/issue19846
ENV LANG=C.UTF-8
