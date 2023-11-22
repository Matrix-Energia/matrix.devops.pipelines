FROM node:18-buster as builder
RUN mkdir -p /usr/src/next-nginx
WORKDIR /usr/src/next-nginx
COPY . .
RUN npm install && npm ci && npm run build
RUN rm .env
EXPOSE 3000
CMD ["npm", "start"]
