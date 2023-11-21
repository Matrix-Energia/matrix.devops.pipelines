FROM nginx:stable-alpine
ADD nginx.conf /etc/nginx
RUN rm -rf /etc/nginx/conf.d/default.conf
ADD default.conf /etc/nginx/conf.d
WORKDIR /usr/share/nginx/html
RUN rm -rf ./* 
COPY . ./
CMD [ "nginx", "-g", "daemon off;" ]
