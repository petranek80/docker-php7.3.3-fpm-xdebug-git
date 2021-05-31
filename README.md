# docker-php7.3.3-fpm-xdebug-git
added git support

Dockerfile for PHP 7.3.3 fpm

* with PDO (MySQL client)
* with xdebug (client_host=127.0.0.1, client_port=9003, idekey="PHPSTORM")
* with git (clone in composer.phar)

## docker hub link

https://hub.docker.com/repository/docker/petranek80/php7.3.3-fpm-xdebug-git

### 1. add PHP docker image to docker-compose.yml file

```
  php:
    image: petranek80/php7.3.3-fpm-xdebug-git
    volumes:
      - ".:/var/www/html"
      - "./etc/php/php.ini:/usr/local/etc/php/conf.d/custom.php.ini"
```
      

### 2. create PHP config file in project folder

/etc/php/php.ini
```
[pdo_mysql]
pdo_mysql.default_socket=/var/run/mysqld/mysqld.sock
```
      
