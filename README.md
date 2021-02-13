# Laravel apache 7.4

`FROM php:7.4.1-apache`

# Start Service

```
docker run -dit \
--name sikuda \
--link db1:mysql \
--restart unless-stopped \
--user 1000:1000 \
-v /opt/mydir:/var/www/html \
-v /opt/cert:/cert:ro \
-p 8090:80 \
-p 8091:443 \
-e SERVER_NAME=mydomain.co \
-e EMAIL_ADMIN=mydomain.co \
-e SSL_CERT_FILE=/cert/my.pem \
-e SSL_CERT_KEY=/cert/my.key \
akbartk/laravel74:latest
```

Exec
```
docker exec -it MyApp bash
```
```
cd /var/www/html \
&& composer install
```