FROM registry.access.redhat.com/ubi8/nodejs-14
WORKDIR /usr/src/app
COPY package*.json /usr/src/app/
USER root
RUN npm install
COPY . .
RUN chown -R 1001:0 /usr/src/app/ && chmod -R ug+rwx /usr/src/app/
USER 1001
EXPOSE 8080
CMD [ "index.js" ]
