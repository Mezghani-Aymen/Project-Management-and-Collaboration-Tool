# Use the official Node.js 19 LTS image as the base image
FROM node:19  

# Set the working directory inside the container
WORKDIR /app

# Install the NestJS CLI globally
RUN npm install -g @nestjs/cli

# Copy package.json and package-lock.json files to the container
COPY package*.json ./

COPY tsconfig.build.json ./
COPY tsconfig.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code to the container
COPY . .

# Expose the application port
EXPOSE 3000

# Set the command to run the application
CMD ["npm", "run", "start:dev"]
