# TYPO3 Example

Docker driven. Start the environment with:

`docker stack deploy --compose-file=$(pwd)/docker-compose.yml example`

or with docker-compose:

`docker-compose up`

The site is now accessible at http://localhost:8088

## TYPO3 Admin:

http://localhost:8088/typo3

User: admin
Password: admin0123

## SQL Dump

A SQL Dump is always imported on startup. It is located under ``./docker/dumps/latest.sql.gz``
