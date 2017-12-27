mysql -u root -p -h127.0.0.1 -P 3306


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




 mysql -u dbuser -p -h127.0.0.1 -P 3306 --database=exampleDb


docker-compose up

docker-compose rm -v


http://localhost:8080/
