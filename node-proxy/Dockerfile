FROM nginx

COPY ./default.conf /etc/nginx/conf.d/default.conf
COPY ./.htpasswd /etc/nginx/.htpasswd
COPY ./ssl/* /etc/ssl/private/

EXPOSE 80 443
