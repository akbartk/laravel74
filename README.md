# Laravel apache 7.4

`FROM php:7.4.1-apache`

# Start Service

```
docker run -dit \
--name MyApp \
--link db0001:mysql \
--restart unless-stopped \
--user 33:33 \
-v ${pwd}:/var/www/html \
-v ${pwd}:/cert \
-p 8080:80 \
-p 8081:443 \
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