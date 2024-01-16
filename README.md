# test_db

Fork [datacharmer/test_db](https://github.com/datacharmer/test_db) for create Docker environment.

## setup

```bash
docker compose up
docker compose exec mysql
$ cd docker-entrypoint-initdb.d
$ mysql < employees_partitioned.sql -u root -p # enter password "password"
...seeding data
```
