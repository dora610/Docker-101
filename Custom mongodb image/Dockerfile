# step 1:
FROM alpine:3.9

# step 2.1: add repo to alpine
RUN echo 'http://dl-cdn.alpinelinux.org/alpine/v3.9/main' >> /etc/apk/repositories
RUN echo 'http://dl-cdn.alpinelinux.org/alpine/v3.9/community' >> /etc/apk/repositories
RUN apk update

# step 2.2: install mongodb
RUN apk add binutils
RUN apk add mongodb=4.0.5-r0

# step 2.3: configure mongodb
VOLUME [ "/data/db" ]
WORKDIR /data
EXPOSE 27017

# RUN apk add isl
# step 3: set default command -- optional
CMD [ "mongod" ]