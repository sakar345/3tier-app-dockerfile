FROM registry.access.redhat.com/ubi8/nodejs-14
WORKDIR /usr/src/app
COPY /package*.json /usr/src/app/
RUN yum npm install
COPY . .
EXPOSE 8080
ENTRYPOINT ["./bin/www"]
CMD [ "node" ]
