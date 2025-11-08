FROM node:18-alpine
WORKDIR /usr/src/app
COPY package*.json ./
# Use npm ci when package-lock.json exists for reproducible builds; fallback to npm install.
RUN if [ -f package-lock.json ]; then npm ci --only=production; else npm install --only=production; fi
COPY . .
# Expose the port the service listens on
EXPOSE 3000
# Start the app
CMD ["npm", "start"]
