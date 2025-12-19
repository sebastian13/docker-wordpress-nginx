# Docker Wordpress Nginx

This is a best practise docker-compose file to start a [WordPress Docker Container](https://hub.docker.com/_/wordpress/).

- Defined wordpress alpine fpm containers and latest nginx are used
- The maximum upload file size is set to 64MB
- Expires headers for static content are set
- Enables Brotli & GZIP

## How to use

```bash
git clone https://github.com/sebastian13/docker-wordpress-nginx.git .

# Copy the example files and set all req. variables
cp default_env .env
cp default_env-wordpress .env-wordpress
cp default_cron cron

# Start the containers
docker-compose up -d
```

### Update
To get the most recent version of this repo run:

```bash
git fetch --all && \
git reset --hard origin/master && \
docker-compose pull && \
docker-compose down && \
docker-compose up -d
```