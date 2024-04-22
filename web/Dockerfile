# Use the official Node.js image as a base
FROM node:16-slim

# Set environment variables
ENV VITE_HOST=0.0.0.0
ENV VITE_PORT=5173
ENV API_HOST='http://api.avatar.d.shuhariko.com.ar'

# Set the working directory in the container
WORKDIR /app

# Copy package.json and yarn.lock to the working directory
COPY package.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code to the working directory
COPY . .

# Expose the port the app runs on
EXPOSE $VITE_PORT

# Run the application
CMD ["npm", "run", "dev"]
