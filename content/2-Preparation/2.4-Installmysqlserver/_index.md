---
title : "Installing MySQL Server"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 2.4 </b> "
---

#### Installing MySQL Server

1. After successfully logging in with your user/password, you can download MySQL server on EC2.

```
sudo apt-get install mysql-server -y
```

![Application Migration Service](/images/3/00013.png?featherlight=false&width=90pc)

2. Check the version of MySQL that has been installed.

```
mysql --version
```
![Application Migration Service](/images/3/00014.png?featherlight=false&width=90pc)

3. You will connect to the MySQL server and set a password for the user.

```
sudo mysql -u root -p
```
Then, set a password for the root user.

```
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '123456789@Aws';

FLUSH PRIVILEGES;

exit;
```
![Application Migration Service](/images/3/00015.png?featherlight=false&width=90pc)


4. Perform some interactive commands with MySQL

```
sudo mysql
```

To view a list of databases:

```
SHOW DATABASES;
```

To create a database:

```
CREATE DATABASE awsfcjuser;
```

Then, use the database:

```
USE awsfcjuser;
```

![Application Migration Service](/images/3/00017.png?featherlight=false&width=90pc)

5. Execute the creation of a table in the AWSFCJUSER database using the CREATE TABLE command.

```
CREATE TABLE `awsfcjuser`.`user` ( `id` INT NOT NULL AUTO_INCREMENT , `first_name` VARCHAR(45) NOT NULL , `last_name` VARCHAR(45) NOT NULL , `email` VARCHAR(45) NOT NULL , `phone` VARCHAR(45) NOT NULL , `comments` TEXT NOT NULL , `status` VARCHAR(10) NOT NULL DEFAULT 'active' , PRIMARY KEY (`id`)) ENGINE = InnoDB;
```

![Application Migration Service](/images/3/00018.png?featherlight=false&width=90pc)

6. Verify that the table is created using the DESCRIBE command:

```
DESCRIBE user;
```
![Application Migration Service](/images/3/00019.png?featherlight=false&width=90pc)

7. Insert information into a table using the INSERT INTO statement:

```
INSERT INTO `user`
(`id`, `first_name`, `last_name`, `email`, `phone`, `comments`, `status`)
VALUES
(NULL, 'Amanda', 'Nunes', 'anunes@ufc.com', '012345 678910', '', 'active'),
(NULL, 'Alexander', 'Volkanovski', 'avolkanovski@ufc.com', '012345 678910', '', 'active'),
(NULL, 'Khabib', 'Nurmagomedov', 'knurmagomedov@ufc.com', '012345 678910', '', 'active'),
(NULL, 'Kamaru', 'Usman', 'kusman@ufc.com', '012345 678910', '', 'active'),
(NULL, 'Israel', 'Adesanya', 'iadesanya@ufc.com', '012345 678910', '', 'active'),
(NULL, 'Henry', 'Cejudo', 'hcejudo@ufc.com', '012345 678910', '', 'active'),
(NULL, 'Valentina', 'Shevchenko', 'vshevchenko@ufc.com', '012345 678910', '', 'active'),
(NULL, 'Tyron', 'Woodley', 'twoodley@ufc.com', '012345 678910', '', 'active'),
(NULL, 'Rose', 'Namajunas ', 'rnamajunas@ufc.com', '012345 678910', '', 'active'),
(NULL, 'Tony', 'Ferguson ', 'tferguson@ufc.com', '012345 678910', '', 'active'),
(NULL, 'Jorge', 'Masvidal ', 'jmasvidal@ufc.com', '012345 678910', '', 'active'),
(NULL, 'Nate', 'Diaz ', 'ndiaz@ufc.com', '012345 678910', '', 'active'),
(NULL, 'Conor', 'McGregor ', 'cmcGregor@ufc.com', '012345 678910', '', 'active'),
(NULL, 'Cris', 'Cyborg ', 'ccyborg@ufc.com', '012345 678910', '', 'active'),
(NULL, 'Tecia', 'Torres ', 'ttorres@ufc.com', '012345 678910', '', 'active'),
(NULL, 'Ronda', 'Rousey ', 'rrousey@ufc.com', '012345 678910', '', 'active'),
(NULL, 'Holly', 'Holm ', 'hholm@ufc.com', '012345 678910', '', 'active'),
(NULL, 'Joanna', 'Jedrzejczyk ', 'jjedrzejczyk@ufc.com', '012345 678910', '', 'active');
```
![Application Migration Service](/images/3/00020.png?featherlight=false&width=90pc)

8. Use the SELECT command to display the table:

```
SELECT * FROM user;
```
- Use the exit command to exit.
