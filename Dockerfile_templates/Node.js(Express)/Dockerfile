# Use an official Node.js runtime as a parent image
FROM node:20-alpine

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json first to leverage Docker's caching
# This ensures npm install is only re-run if dependencies change
COPY package*.json ./

# Install application dependencies
RUN npm install

# Copy the rest of the application source code
COPY . .

# Expose the port your application will run on
EXPOSE 3000

# Define the command to run your application
CMD [ "node", "server.js" ]