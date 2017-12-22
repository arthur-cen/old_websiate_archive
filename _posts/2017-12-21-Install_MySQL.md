---
layout: post
title: Setup MySQL database on Mac OSX
author: Shengrui Cen
---

## Install MySQL database via Homebrew

1. Get most recent commit of `gc_game` from remote
```
$ git pull origin master
```
2. If not already, install `HomeBrew`
```
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
3. Check all `mysql` dependencies by
```
$ brew info mysql
```
4. If not all requirements met, run following command to install requirement, replace `PACKAGE_NAME` with required dependency
```
$ brew install PACKAGE_NAME
```
5. After installing all dependencies, run:
```
$ brew install mysql
```
6. Read the installation log to learn how to start mysql, and how to setup. Or if you're lazy, just run
```
$ brew services start mysql
```
Run this to see all listed services by HomeBrew
```
$ brew services list
```

## Create a new user, and grant privilege to access a database
1. Login mysql database (with root access), after entering your root password
```
$ mysql -u root -p
```
2. In this example we create an empty database `my_db`
```
mysql> CREATE DATABASE my_db;
```
3. Let's create a user to access this database instead of logging in all the time with root privilege.
```
mysql> CREATE USER 'user_1' IDENTIFIED BY 'user_1_pwd';
```
The String followed by the clause `IDENTIFIED BY` is the password of the new user.
4. Grant privilege to the new user, here, 'user_1'.
```
mysql> GRANT ALL PRIVILEGES ON my_db.* TO 'user_1';
```

## Import Database to mysql
1. It is easier to do this with a GUI. Download a light-weight database GUI of your choice, here I used Sequel Pro.
2. Login via Socket as *gc_user1*, as in previous example, and select database *my_db*
3. Go to File -> Import, and select the database file, make sure format is SQL, then click open.

## Serve Creator on localhost
1. Go to gc_game/server
```
$ node server.js
```
2. Now creator is served on localhost:3000