FROM node:18-alpine
WORKDIR /usr/src/app
COPY package*.json ./
RUN if [ -f package-lock.json ]; then npm ci --only=production; else npm install --only=production; fi
COPY . .
EXPOSE 3001
CMD ["npm", "start"]
