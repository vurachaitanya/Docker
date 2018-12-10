FROM ubuntu:latest
MAINTAINER Chaitanya Vura (vurachaitanya@gmail.com)
RUN apt-get update || apt-get install -y nginx
ENTRYPOINT ["/usr/sbin/nginx","-g","daemon off;"]
EXPOSE 80
