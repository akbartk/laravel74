# Laravel apache 7.4 .

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
akbartk/laravel74:latest
```

Exec
```
docker run - -it MyApp bash
```
```
cd /var/www/html \
&& composer install
```
```
docker run --rm akbartk/laravel74:latest composer install
```