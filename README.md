skeleton-maven-liquibase
=======

Skeleton project for maven/liquibase database initialisation. This uses mysql but could easily be changed to another database. For convenience,
I have also included a docker-compose file so you can start a local mysql instance to run liquibase against.

How do run it?
=====

Start docker using `docker-compose up`. See the docker compose yaml file for container configuration.

The docker container should create a schema named `exampleDb` so you can either connect to that as root or as the user it also creates:

* `mysql -u root -p -h127.0.0.1 -P 3306`
* `mysql -u dbuser -p -h127.0.0.1 -P 3306 --database=exampleDb`


Then you can show the databases to confirm it has set things up:

```
mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| exampleDb          |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
5 rows in set (0.00 sec)
```


Alternatively, you can go to http://localhost:8080 to view the adminer console for the DB.


To create the database schema, add your updates in the changelog file, then run `mvn process-resources`

If you change anything in the docker compose file, be sure to clear the containers before restarting so compose doesn't cache configuration, `docker-compose rm -v`


Suggestions
========
Any suggestions, please find me on twitter @jameselsey1986
