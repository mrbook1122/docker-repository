# mysql

> docker run --name mysql -v mysql:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=123456 --publish 3306:3306 -d --network my-net --restart always mysql