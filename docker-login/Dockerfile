FROM nickistre/ubuntu-lamp:latest
ADD login/ /var/www/html
ADD service_start.sh /
RUN service mysql start && mysql -uroot -e"create database member;use member;create table user(id int auto_increment,user varchar(100),password varchar(100),primary key (id));insert into user(user,password) values ('test1','5a105e8b9d40e1329780d62ea2265d8a');insert into user(user,password) values ('test2','ad0234829205b9033196ba818f7a872b');insert into user(user,password) values ('test3','8ad8757baa8564dc136c1e07507f4a98');insert into user(user,password) values ('1test','ba88c155ba898fc8b5099893036ef205');insert into user(user,password) values ('2test','7cbab5cea99169139e7e6d8ff74ebb77');insert into user(user,password) values ('3test','flag{ca820ad57809f62eb7b4d13f5d4371a0}');"

EXPOSE 80 3306

CMD ["/start.sh"]
