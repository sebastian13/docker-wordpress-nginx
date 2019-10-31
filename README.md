# Docker Wordpress Nginx

This is a best practise docker-compose file to start a [WordPress Docker Container](https://hub.docker.com/_/wordpress/).

- Latest wordpress:fpm and latest nginx are used
- The maximum upload file size is set to 64MB
- Expires headers for static content are set
- Nginx Cache is used for dynamic files
- Enables GZIP

## How to use

```bash
git clone https://github.com/sebastian13/docker-wordpress-nginx.git .
echo "MYSQL_DATABASE=example" >> .env
echo "MYSQL_ROOT_PASSWORD=123456" >> .env
docker-compose up -d
```