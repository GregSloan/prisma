ARG SECRET_KEY

FROM nginx:alpine
COPY . /usr/share/nginx/html/a/
COPY ./ssl/* /etc/ssl/certs/
COPY ./default.conf /etc/nginx/conf.d/default.conf
EXPOSE 443
