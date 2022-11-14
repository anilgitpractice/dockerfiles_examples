# this is the docker file for building the hipache image
FROM komljen/nodejs

MAINTAINER anil anilsurfexel@gmail.com

RUN \
     npm install hipache -g

COPY config.json config.json
COPY start.sh start.sh

RUN rm /usr/sbin/policy-rc.d
CMD ["/start.sh"]


EXPOSE 80
