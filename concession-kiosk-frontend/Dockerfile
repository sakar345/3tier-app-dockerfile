FROM registry.access.redhat.com/ubi8/nodejs-14
RUN mkdir -p /usr/src/app && chown -R node:node /usr/src/app
WORKDIR /usr/src/app
COPY /package*.json /usr/src/app/
USER node
RUN npm install
COPY --chown=node:node . .
EXPOSE 8080
ENTRYPOINT ["./bin/www"]
CMD [ "node" ]
