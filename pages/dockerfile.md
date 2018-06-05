---
layout: page
title: "Dockerfile"
meta_title: "Dockerfile"
subheadline: ""
teaser: ""
permalink: "/dockerfile/"
---


An example of GUDHI installation with Docker:

```Docker
# Image de base
FROM ubuntu:16.04

# Installation des dependances
RUN apt-get update

RUN apt-get install -y curl make cmake g++ libboost-all-dev libeigen3-dev libgmp3-dev libmpfr-dev libtbb-dev locales \
python3 ipython3 python3-pip python3-pytest python3-tk libfreetype6-dev pkg-config

RUN apt-get -y upgrade 
RUN rm -rf /var/lib/apt/lists/*

RUN pip3 install Cython sphinx sphinxcontrib-bibtex matplotlib numpy

# Changement du repertoire courant
WORKDIR /gudhi

RUN locale-gen en_US.UTF-8

CMD curl -LO "https://github.com/CGAL/cgal/releases/download/releases%2FCGAL-4.11/CGAL-4.11.tar.xz" \
&& tar xf CGAL-4.11.tar.xz && cd CGAL-4.11 \
&& cmake -DCGAL_HEADER_ONLY=ON . && make all install && cd .. \
&& curl -LO "https://gforge.inria.fr/frs/download.php/file/37362/2018-01-31-09-25-53_GUDHI_2.1.0.tar.gz" \
&& tar xf 2018-01-31-09-25-53_GUDHI_2.1.0.tar.gz && cd 2018-01-31-09-25-53_GUDHI_2.1.0 \
&& mkdir build && cd build && cmake -DPython_ADDITIONAL_VERSIONS=3 .. \
&& export PYTHONPATH="/root/2018-01-31-09-25-53_GUDHI_2.1.0/build/cython:$PYTHONPATH" && make all test
```
