# # Use an official Node.js image as the base image
# FROM node:14-alpine

# # Set the working directory
# WORKDIR /app

# # Copy the package.json and package-lock.json
# COPY package*.json ./

# # Install dependencies
# RUN npm install

# # Copy the rest of the application code
# COPY . .

# # Expose the port the app runs on
# EXPOSE 3000

# # Start the application
# CMD ["npm", "start"] 

# # ["npm", "index.js"]

FROM node:latest

WORKDIR /backend

COPY package*.json ./

RUN npm install

FROM node:alpine 

COPY . /backend

EXPOSE 3001

CMD ["node", "index.js"]
