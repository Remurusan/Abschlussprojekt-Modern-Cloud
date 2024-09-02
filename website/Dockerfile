# Base image
FROM node:18-alpine

# Set the working directory
WORKDIR /app

# Copy package.json and install dependencies
COPY package.json ./
RUN npm install

# Copy the application code
COPY . .

# Build the app for production
RUN npm run build

# Serve the app using a lightweight web server
RUN npm install -g serve
CMD ["serve", "-s", "build"]

# Expose the port
EXPOSE 3000
