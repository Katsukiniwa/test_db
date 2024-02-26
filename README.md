# test_db

Fork [datacharmer/test_db](https://github.com/datacharmer/test_db) for create Docker environment.

## setup

```bash
docker compose up
docker compose exec mysql bash
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

## connect from local

use [mycli](https://www.mycli.net/)

```bash
$ mycli mysql://root@localhost:3306/employees
Password:
MySQL
mycli 1.27.0
Home: http://mycli.net
Bug tracker: https://github.com/dbcli/mycli/issues
Thanks to the contributor - mrdeathless
MySQL root@localhost:employees> select * from departments limit 1;
+---------+------------------+
| dept_no | dept_name        |
+---------+------------------+
| d009    | Customer Service |
+---------+------------------+

1 row in set
Time: 0.013s
MySQL root@localhost:employees>
```
