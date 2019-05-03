# RecommenDr

生徒たちがオススメの教授を発表し合う場所

## versions
ruby 2.6.2<br>
sinatra 2.0.5<br>
sinatra-contrib 2.0.5<br>
pg 1.1.4<br>

## gem
```$ gem install sinatra sinatra-contrib pg```

## DB

create db <br>
```$ createdb recommendr```

create users table <br>
```
create table users (id serial primary key, name varchar(20) not null, password text not null, image text default 'default_user_image.jpg');
```

create rewiews table <br>
```
create table reviews (id serial primary key, title varchar(20) not null, contents text not null, user_id integer, doctor_id integer, star integer);
```

create doctors table <br>
```
create table doctors (id serial primary key, name varchar(20), introduction text, belonging varchar(30), image text default 'default_user_image.jpg', class_id integer);
```

create classes table <br>
```
create table classes (id serial primary key, name varchar(20), introduction text, doctor_id integer);
```

create admin table <br>
```
create table admin (id serial primary key, name varchar(20), password varchar(30), email varchar(50));
```
