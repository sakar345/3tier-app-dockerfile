FROM registry.access.redhat.com/ubi8/nodejs-14
WORKDIR /usr/src/app
COPY /package*.json /usr/src/app/
USER root
RUN npm install
COPY  . .
EXPOSE 8080
ENTRYPOINT ["./bin/www"]
USER node
CMD [ "node" ]
