# test_db

Fork [datacharmer/test_db](https://github.com/datacharmer/test_db) for create Docker environment.

## setup

```bash
docker compose up
docker compose exec mysql
$ cd docker-entrypoint-initdb.d
$ mysql < employees_partitioned.sql -u root -p # enter "password"
Enter password:
INFO
CREATING DATABASE STRUCTURE
INFO
storage engine: InnoDB
INFO
LOADING departments
INFO
LOADING employees
INFO
LOADING dept_emp
INFO
LOADING dept_manager
INFO
LOADING titles
INFO
LOADING salaries
data_load_time_diff
00:00:56
```
