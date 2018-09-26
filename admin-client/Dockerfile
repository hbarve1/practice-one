
# Base Image
# FROM node:8.12.0-alpine
FROM node:8.12.0

# Set Working Directory
RUN mkdir /home/node/app
WORKDIR /home/node/app

# Expose port
EXPOSE 4200
EXPOSE 49153

# Install and cache app dependencies
COPY package.json /home/node/app/package.json
COPY package-lock.json /home/node/app/package-lock.json

RUN npm install -g @angular/cli@6.2.3
RUN npm install

# Copy App Code
COPY . /home/node/app

# Start Angular App
# NOTE: poll only works for windows => 
## https://stackoverflow.com/questions/44176922/docker-container-doesnt-reload-angular-app
CMD ng serve --watch --host 0.0.0.0 --poll
# CMD ng serve --watch --live-reload --host 0.0.0.0 --poll
