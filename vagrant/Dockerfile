ARG version=20.04
FROM ubuntu:$version
ENV DEBIAN_FRONTEND=noninteractive
WORKDIR /vagrant
RUN apt-get update && apt-get install curl virtualbox  -y &&\
    apt-get update && curl -O https://releases.hashicorp.com/vagrant/2.2.6/vagrant_2.2.6_x86_64.deb &&\
    apt-get install ./vagrant_2.2.6_x86_64.deb && apt-get clean && rm -rf vagrant_2.2.6_x86_64.deb
CMD ["/bin/bash"]