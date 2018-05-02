[![Docker Pulls](https://img.shields.io/docker/pulls/zaherg/php-and-nginx-xdebug.svg)](https://hub.docker.com/r/zaherg/php-and-nginx-xdebug/) [![](https://images.microbadger.com/badges/image/zaherg/php-and-nginx-xdebug.svg)](https://microbadger.com/images/zaherg/php-and-nginx-xdebug "Get your own image badge on microbadger.com") [![](https://images.microbadger.com/badges/version/zaherg/php-and-nginx-xdebug.svg)](https://microbadger.com/images/zaherg/php-and-nginx-xdebug "Get your own version badge on microbadger.com") [![](https://images.microbadger.com/badges/commit/zaherg/php-and-nginx-xdebug.svg)](https://microbadger.com/images/zaherg/php-and-nginx-xdebug "Get your own commit badge on microbadger.com")

# PHP, Nginx & Xdebug Docker image

This image was built based on the scripts that I have found at [docker-alpine-micro](https://github.com/nimmis/docker-alpine-micro) , and with the help of his [docker-utils](https://github.com/nimmis/docker-utils) script I was able to build my own image.

This is still new/simple docker image which will have:

1. PHP7.2
2. Nginx
3. Crond
4. rsyslogd

## PHP Modules

[PHP Modules]
1. Core
1. ctype
1. curl
1. date
1. dom
1. fileinfo
1. filter
1. ftp
1. gd
1. hash
1. iconv
1. intl
1. json
1. libxml
1. mbstring
1. mysqlnd
1. openssl
1. pcre
1. PDO
1. pdo_mysql
1. pdo_pgsql
1. pdo_sqlite
1. pgsql
1. Phar
1. posix
1. readline
1. redis
1. Reflection
1. session
1. SimpleXML
1. sodium
1. SPL
1. sqlite3
1. standard
1. tokenizer
1. xdebug
1. xml
1. xmlreader
1. xmlwriter
1. Zend OPcache
1. zip
1. zlib

[Zend Modules]
1. Xdebug
1. Zend OPcache

## Configuration

By default xdebug is enabled, to disable it you need to create a `.env` file which should contain the following variables, but remember to change the value based one what you want to achieve:

```
PHP_XDEBUG_DEFAULT_ENABLE=0
PHP_XDEBUG_REMOTE_ENABLE=0
PHP_XDEBUG_REMOTE_HOST=127.0.0.1
PHP_XDEBUG_REMOTE_PORT=9001
PHP_XDEBUG_REMOTE_AUTO_START=0
PHP_XDEBUG_REMOTE_CONNECT_BACK=0
PHP_XDEBUG_IDEKEY=docker
PHP_XDEBUG_PROFILER_ENABLE=0
PHP_XDEBUG_PROFILER_OUTPUT_DIR=/tmp
```

Then run the docker and specify the env file that you have created like this

```
docker run --env-file .env -p 80:80 zaherg/php-and-nginx-xdebug
```

## GD information

```
array(12) {
  'GD Version' =>
  string(26) "bundled (2.1.0 compatible)"
  'FreeType Support' =>
  bool(false)
  'GIF Read Support' =>
  bool(true)
  'GIF Create Support' =>
  bool(true)
  'JPEG Support' =>
  bool(false)
  'PNG Support' =>
  bool(true)
  'WBMP Support' =>
  bool(true)
  'XPM Support' =>
  bool(false)
  'XBM Support' =>
  bool(true)
  'WebP Support' =>
  bool(false)
  'BMP Support' =>
  bool(true)
  'JIS-mapped Japanese Font Support' =>
  bool(false)
}
```