FROM alpine:3.7

RUN apk add --update nginx && rm -rf /var/cache/apk/*
RUN mkdir -p /tmp/nginx/client-body
RUN mkdir -p /run/nginx/ && touch /run/nginx/nginx.pid 

ADD ./conf/nginx/vhost.conf /etc/nginx/conf.d/default.conf

WORKDIR /var/www

# COPY ./conf/nginx/nginx.conf /etc/nginx/nginx.conf

# EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]