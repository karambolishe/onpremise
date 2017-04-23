# Sentry

## Requirements

 * Docker 1.10.0+
 * Compose 1.6.0+

## Up and Running

1. `mkdir -p data/{sentry,postgres,redis,rabbitmq,redis,elasticsearch}`
2. `docker-compose run --rm web django elastic_template`
3. `docker-compose run --rm web config generate-secret-key` - Generate a secret key.
    Add it to `docker-compose.yml` in `base` as `SENTRY_SECRET_KEY`.
4. `docker-compose run --rm web upgrade`
5. `docker-compose up -d`
6. Open `127.0.0.1:80`
