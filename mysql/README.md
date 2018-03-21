# mysql-docker
mysql-docker

### usage
run by docker 
```
docker run -p 3306:3306 --name mysql_db_1 -v ./conf/my.cnf:/etc/mysql/my.cnf -v ./logs:/var/log/mysql/ -v ./data:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=root -d mysql:5.6
```

run by docker-compose 
```
docker-compose up
```

use mysql-client 
```
docker run --rm -ti --link mysql_db_1:db mysql:5.6 mysql -h db -uroot -p
```