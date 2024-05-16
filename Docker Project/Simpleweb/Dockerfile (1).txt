#Specify Base Image
FROM node:18-alpine

#Create working directory
WORKDIR /usr/app

#copy file into container
COPY ./ ./

#Install dependancies
RUN npm install

#copy all other files into container
COPY ./ ./

#Start server

CMD ["npm","start"]