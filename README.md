# TYPO3 Example

Docker driven. Start the environment with:

`docker stack deploy --compose-file=$(pwd)/docker-compose.yml example`

or with docker-compose:

`docker-compose up`

## Composer packages

RUn the following command INSIDE the php container to install all required packages:

``docker exec -ti -w /var/www/html/typo3_app $(docker ps --filter name=php --format {{.ID}}) php composer.phar install``

After installation the site should be accessible at http://localhost:8088

## TYPO3 Admin:

http://localhost:8088/typo3

User: admin
Password: admin0123

## SQL Dump

A SQL Dump is always imported on startup. It is located under ``./docker/dumps/latest.sql.gz``
