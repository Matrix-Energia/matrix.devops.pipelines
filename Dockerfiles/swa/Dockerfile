FROM nginx:stable-alpine
ADD nginx.conf /etc/nginx
WORKDIR /usr/share/nginx/html
RUN rm -rf ./* 
ADD TMP_OUT  ./
COPY .env ./
RUN source /usr/share/nginx/html/.env
RUN apk add vim
CMD [ "nginx", "-g", "daemon off;" ]
