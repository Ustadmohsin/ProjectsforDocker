# Use official Node image
FROM node:20

# Set working directory
WORKDIR /app

# Copy package.json and install dependencies
COPY package*.json ./

RUN npm install --prefer-offline

# Copy source files
COPY . .

# Copy env file
COPY .env.sample .env

# Expose port and start server
EXPOSE 5000
CMD ["npm", "start"]
