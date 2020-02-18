# mysql

> docker run --name mysql -v mysql:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=123456 --publish 3306:3306 -d --network my-net --restart always mysql

# mysql windows上导入sql文件

> docker exec -i some-mysql sh -c "exec mysql -uroot -p$MYSQL_ROOT_PASSWORD" < /some/path/on/your/host/all-databases.sql

此命令必须在cmd中执行