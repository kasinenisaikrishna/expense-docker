# taking alpine base os to reduce the size of an image
FROM node:20-alpine
EXPOSE 8080
ENV DB_HOST="mysql"
# adding expense user and expense group to restrict running the file with root privileges the syntax used below we will get fron search how do i add a user when I am using alpine as base image
RUN addgroup -S expense && adduser -S expense -G expense
RUN mkdir /opt/server
# to change the folder ownership to expense
RUN chown -R expense:expense /opt/server
WORKDIR /opt/server
COPY package.json .
COPY *.js .
RUN npm install
# To make the file to run with expense normal user from the below lines
USER expense
CMD ["node", "index.js"]

# Before best practices implemented
# FROM node:20
# EXPOSE 8080
# ENV DB_HOST="mysql"
# RUN mkdir /opt/server
# WORKDIR /opt/server
# COPY package.json .
# COPY *.js .
# RUN npm install
# CMD ["node", "index.js"]