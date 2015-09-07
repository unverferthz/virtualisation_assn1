#Version 0.0.1
FROM ubuntu:14.04
MAINTAINER Zane Unverferth "unverferthz@gmail.com"
RUN apt-get update
VOLUME ["/var/www/html"]
ADD index.html /var/www/html/
ENTRYPOINT [ "/bin/sh", "-c", "while true; do echo im a datacontainer mate; sleep 60; done" ]
