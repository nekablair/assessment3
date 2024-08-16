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

# # Build the frontend
# RUN npm run build

# # Expose the port the app runs on
# EXPOSE 3001

# # Serve the frontend
# CMD ["npm", "start"]

FROM node:latest

WORKDIR /frontend

COPY package*.json ./

RUN npm install

FROM node:alpine

COPY index.js /usr/share/nginx/html

EXPOSE 3000

# CMD ["npm", "start"]
CMD ["node", "index.js"]