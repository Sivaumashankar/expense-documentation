# MySQL
we r using customized instance ami so sql running otherwise we have to install mysql repos by default it not work it uses mariadb

Developer has chosen the database MySQL. Hence, we are trying to install it up and configure it.

**Versions of the DB Software you will get context from the developer, Meaning we need to check with developer.**

Install MySQL Server 8.0.x

```
dnf install mysql-server -y
```

Start MySQL Service

```
systemctl enable mysqld
```
```
systemctl start mysqld
```

Next, We need to change the default root password in order to start using the database service. Use password ExpenseApp@1 or any other as per your choice.

```
we setting password so if u want to connect sql server u can use ur passwword not default one using ip and pwd u can connect
mysql_secure_installation --set-root-pass ExpenseApp@1
```

## Verification

We can check data by using client package called mysql.

Usually command to connect mysql server is

``` #no need to excute this command as ur in sql server u have to use if u want to acess sql server from outside server within the server no need
mysql -h <host-address> -u root -p<password>
```

But if your client and server both are in a single server, you can simply issue.

```
mysql #now u rin sql client
```use mysql

Once you got mysql prompt, you can use below command to check schemas/databases exist.

```
show databases;
use sys
```

Once you are in particular schema, you can get the list of tables.

```
show tables;
```

You can get entries of a table using

```
select * from <table_name>; hostsummary like that
```
