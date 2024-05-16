#specify base image
FROM alpine

#Create a working directory
WORKDIR /user/app

#install redis in apline
RUN apk add --update redis

#start the redis server
CMD ["redis-server"]