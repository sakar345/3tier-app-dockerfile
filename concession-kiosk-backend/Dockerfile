# Use of redhat ubi/nodejs for base image
FROM registry.access.redhat.com/ubi8/nodejs-14
# Create a working dir.
WORKDIR /usr/src/app
# Copy files to our new dir
COPY package*.json /usr/src/app/
# Change permission to run the command
USER root
# Run the below command
RUN npm install && npm audit fix
# Copy all the files from the current directory to the new dir
COPY . .
# Change ownership to the dir so we could access it using the non-root user on the container.
RUN chown -R 1001:0 /usr/src/app/ && chmod -R ug+rwx /usr/src/app/
# Setting non-root user
USER 1001
# Expose port for the container
EXPOSE 8080
# Command to run
CMD [ "node", "index.js" ]
