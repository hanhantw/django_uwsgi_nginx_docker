FROM nginx:alpine

# COPY index.html /usr/share/nginx/html
# COPY site.conf /etc/nginx/conf.d/default.conf

COPY nginx.conf /etc/nginx/

# Create 'messages' file used from 'logrotate'
# RUN touch /var/log/messages

# Copy 'logrotate' config file
# COPY logrotate/nginx /etc/logrotate.d/

# RUN apk update \
#     && apk upgrade \
#     && apk add --no-cache bash \
#     && adduser -D -H -u 1000 -s /bin/bash www-data

# Set upstream conf and remove the default conf
RUN echo "upstream php-upstream { server ${PHP_UPSTREAM_CONTAINER}:${PHP_UPSTREAM_PORT}; }" > /etc/nginx/conf.d/upstream.conf \
    && rm /etc/nginx/conf.d/default.conf

CMD ["nginx", "-g", "daemon off;"]

EXPOSE 80 443