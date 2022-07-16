ARG version=20.04
FROM ubuntu:$version
LABEL Author=DevOps
ENV DEBIAN_FRONTEND=noninteractive
WORKDIR /var/www/html
VOLUME /var/log/apache2
EXPOSE 80
CMD ["/usr/sbin/apache2ctl","-D","FOREGROUND"]
RUN apt-get update && apt-get install apache2 git -y &&  apt-get clean
ADD app.tar.gz .