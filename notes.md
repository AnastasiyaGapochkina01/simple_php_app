# Приложение, выводящее табличку автомобилей и позволяющее добавлять автомобили
### Клонирование репозитория
```
$ git clone https://github.com/AnastasiyaGapochkina01/simple_php_app.git /var/www/simple_app
```
### Создание БД
```
$ mysql -uroot -p
> create database simple_app;
> use simple_app;
> create table cars (id int, model varchar(20), license varchar(20), color varchar(20));
> create user 'php'@'%' identified by 'phppasswd';
> grant usage on *.* to 'php'@'%';
> grant select, insert on simple_app.* to 'php'@'%';
> flush privileges;
> exit
$ mysql -uroot -p simple_app < sample_data.sql
```
### Конфигурация nginx
```
$ sudo cp simple_app /etc/nginx/sites-available/simple_app
$ sudo ln -s /etc/nginx/sites-available/simple_app /etc/nginx/sites-enabled
$ sudo nginx -t
$ sudo nginx -s reload
```
Результат работы:
по адресу машины должно открываться

