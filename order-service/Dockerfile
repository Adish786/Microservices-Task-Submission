FROM node:18-alpine
# Set working directory
WORKDIR /usr/src/app
# Copy package files
COPY package*.json ./
# Install production dependencies
RUN if [ -f package-lock.json ]; then npm ci --only=production; else npm install --only=production; fi
# Copy source code
COPY . .
# Expose service port
EXPOSE 3002
# Start service
CMD ["npm", "start"]
