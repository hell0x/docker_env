FROM nginx:1.18

RUN mv /etc/nginx/conf.d /etc/nginx/conf.d.bak
COPY ../conf.d /etc/nginx/conf.d/
COPY ./nginx/conf.d /etc/nginx/conf.d

VOLUME ["/var/www"]