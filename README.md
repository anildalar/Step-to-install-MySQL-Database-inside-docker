# Step-to-install-MySQL-Database-inside-docker
Step to install MySQL Database inside docker


docker run -it -d -p 3306:3306 --name uc1 ubuntu:latest

docker container exec -it /bin/bash

apt update
apt list --upgradable
apt upgrade -y

apt install mysql-server -y
service mysql start

service mysql status
mysql


CREATE USER 'anil'@'localhost' IDENTIFIED BY 'anil@123';

CREATE USER 'abhishek'@'%' IDENTIFIED BY 'abhishek@123';

If we want to give all permission then

ALL PRIVILEGES

GRANT ALL PRIVILEGES ON *.* TO 'anil'@'localhost' WITH GRANT OPTION;

GRANT ALL PRIVILEGES ON *.* TO 'abhishek'@'%' WITH GRANT OPTION;

FLUSH PRIVILEGES;

service mysql restart

docker run -it -d -p 3306:3306 --name uc3 uc2


Allow MySQL Server to accept remote request


apt install plocate -y
plocate my.cnf
plocate my.ini
plocate mysqld.cnf


/etc/mysql/my.cnf

apt install vim -y

vim /etc/mysql/mysql.conf.d/mysqld.cnf

[mysqld]
bind-address = 0.0.0.0


service mysql restart


oklabs/mysql8_image1


docker run -it -d -p 4406:3306 --name mysqlcont2 oklabs/mysql8_image1
