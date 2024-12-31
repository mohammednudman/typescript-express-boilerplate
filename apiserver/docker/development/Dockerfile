# Using Lightweight docker image for node
FROM node:20-alpine AS base

# Set Up Working Directory
WORKDIR /usr/src/app

# Copy Package Files
COPY package*.json ./

# Install Dependencies (Including devDependencies)
RUN npm ci --include=dev

# Copy Application Files
COPY . .

# Install Global Dependencies for Development
RUN npm install -g nodemon cross-env

# Expose Port
EXPOSE 3000

# Start the Application
CMD ["npm", "run", "dev"]
