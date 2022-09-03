FROM nginx:1.23-alpine

ENV TZ="Europe/Paris"
RUN cp /usr/share/zoneinfo/Europe/Paris /etc/localtime
RUN echo "Europe/Paris" >  /etc/timezone

COPY ./default.conf /etc/nginx/conf.d/default.conf
RUN mkdir -p /var/www/html

LABEL version="1.4.1-alpine"

EXPOSE 80
