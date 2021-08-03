FROM ubi7/ubi:7.7
WORKDIR /usr/src/app
COPY /package*.json /usr/src/app/
RUN npm install
COPY . .
RUN chown -R 1001:0 /usr/src/app/ && chmod -R ug+rwx /usr/src/app/
USER 1001
EXPOSE 8080
ENTRYPOINT ["./bin/www"]
CMD [ "node" ]
