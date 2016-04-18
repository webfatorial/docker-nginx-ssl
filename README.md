# webfatorial/docker-nginx-ssl

Nginx extended version: provides a version of nginx with ssl (base from marvambass/nginx-ssl-secure) to use with php-fpm.

## Docker Compose example

```
www:
    image: webfatorial/nginx-ssl
    restart: 'yes'
    ports:
        - "80:80"
        - "443:443"
    volumes:
        - ./www:/var/www/html
        - ./nginx-config:/etc/nginx
    links:
        - fpm

```
