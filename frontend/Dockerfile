# Dockerfile for React Frontend
# frontend/Dockerfile
FROM node:18-alpine AS builder
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

RUN npm install -g serve

# Use serve instead of nginx
EXPOSE 3000
CMD ["serve", "-s", "build", "-l", "3001"]
