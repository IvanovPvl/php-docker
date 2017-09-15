## PHP Docker
Development environment for PHP, PostgreSQL and Nginx with Docker.

## Create new project
```bash
git clone https://github.com/IvanovPvl/php-docker.git <project_name>
```

In docker/env.dev set your database environment settings.

```bash
cd <project_name>/docker
docker-compose -f docker-compose.dev.yml up -d
docker-compose -f docker-compose.dev.yml exec -u docker workspace bash
```

For Laravel based projects:
```bash
composer create-project --prefer-dist laravel/laravel <project_name>
mv <project_name>/{.,}* .
rm -d <project_name>
```
