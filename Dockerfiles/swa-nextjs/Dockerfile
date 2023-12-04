FROM node:18-buster as builder
RUN mkdir -p /usr/src/next
WORKDIR /usr/src/next
COPY . .
RUN npm install && npm ci && npm run build
EXPOSE 3000
CMD ["npm", "start"]
