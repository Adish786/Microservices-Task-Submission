FROM node:18-alpine
WORKDIR /usr/src/app
COPY package*.json ./
RUN if [ -f package-lock.json ]; then npm ci --only=production; else npm install --only=production; fi
COPY . .
# Gateway base path used by some projects; always expose gateway port (3003).
ENV PORT=3003
EXPOSE 3003
CMD ["npm", "start"]
