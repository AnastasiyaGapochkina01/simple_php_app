# Приложение, выводящее табличку автомобилей и позволяющее добавлять автомобили

```
> create database simple_app;
> use simple_app;
> create table cars (id int, model varchar(20), license varchar(20), color varchar(20));
> create user 'php'@'%' identified by 'phppasswd';
> grant usage on *.* to 'php'@'%';
> grant select, insert on simple_app.* to 'php'@'%';
> flush privileges;
```
mysql -uroot -p simple_app < sample_data.sql
