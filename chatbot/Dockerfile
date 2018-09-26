
# Base Image
# FROM node:8.12.0-alpine
FROM node:8.12.0

# Set Working Directory
RUN mkdir /app
WORKDIR /app

# Expose port
EXPOSE 80

# Install and cache app dependencies
COPY package.json /app/package.json
COPY package-lock.json /app/package-lock.json

RUN npm install

# Copy App Code
COPY . /app

# Start Angular App
CMD npm run start
