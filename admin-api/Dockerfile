
# Base Image
# FROM node:8.12.0-alpine
FROM node:8.12.0

# Set Working Directory
RUN mkdir /home/node/app
WORKDIR /home/node/app

# Expose port
EXPOSE 80

# Install and cache app dependencies
COPY package.json /home/node/app/package.json
COPY package-lock.json /home/node/app/package-lock.json

RUN npm install

# Copy App Code
COPY . /home/node/app

# Start Angular App
CMD npm run start
