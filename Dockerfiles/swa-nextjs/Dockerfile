FROM nginx:stable-alpine
ADD nginx.conf /etc/nginx
RUN rm -rf /etc/nginx/conf.d/default.conf
ADD default.conf /etc/nginx/conf.d
WORKDIR /usr/share/nginx/html
RUN rm -rf ./* 
ADD TMP_OUT  ./
COPY .env ./
RUN apk add vim
CMD [ "nginx", "-g", "daemon off;" ]
