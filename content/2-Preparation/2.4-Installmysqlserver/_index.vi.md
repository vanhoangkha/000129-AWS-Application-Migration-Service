---
title : "Cài đặt MySQL Server"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 2.4 </b> "
---

#### Cài đặt MySQL Server

1. Sau khi đăng nhập bằng user/password thành công. Bạn có thể tải MySQL server trên EC2.

```
sudo apt-get install mysql-server -y
```

![Application Migration Service](/images/3/00013.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

2. Kiểm tra version MySQL đã tạo.

```
mysql --version
```

![Application Migration Service](/images/3/00014.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

3. Bạn sẽ kết nối vào MySQL server và đặt mật khẩu cho user.

```
sudo mysql -u root -p
```

- Sau đó, thực hiện tạo password cho user root.

```
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '123456789@Aws';

FLUSH PRIVILEGES;

exit;
```

![Application Migration Service](/images/3/00015.png?featherlight=false&width=90pc?featherlight=false&width=90pc)


4. Thực hiện một số lệnh tương tác với MySQL

```
sudo mysql
```

- Thực hiện xem danh sách database:

```
SHOW DATABASE;
```

- Thực hiện tạo database:

```
create database awsfcjuser;
```

- Sau đó sử dụng database:

```
USE  awsfcjuser;
```


![Application Migration Service](/images/3/00017.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

5. Thực hiện tạo bảng trong database awsfcjuser bằng lệnh **CREATE TABLE**

```
CREATE TABLE `awsfcjuser`.`user` ( `id` INT NOT NULL AUTO_INCREMENT , `first_name` VARCHAR(45) NOT NULL , `last_name` VARCHAR(45) NOT NULL , `email` VARCHAR(45) NOT NULL , `phone` VARCHAR(45) NOT NULL , `comments` TEXT NOT NULL , `status` VARCHAR(10) NOT NULL DEFAULT 'active' , PRIMARY KEY (`id`)) ENGINE = InnoDB;

```

![Application Migration Service](/images/3/00018.png?featherlight=false&width=90pc?featherlight=false&width=90pc)


6. Xác minh rằng bảng được tạo bằng lệnh **DESCRIBE**

```
DESCRIBE user;

```

![Application Migration Service](/images/3/00019.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

7. Chèn thông tin vào trong bảng dữ liệu bằng lệnh **INSERT INTO**

```
INSERT INTO `user` 
(`id`, `first_name`,  `last_name`,    `email`,                 `phone`,         `comments`, `status`) VALUES
(NULL, 'Amanda',      'Nunes',        'anunes@ufc.com',        '012345 678910', '',          'active'),
(NULL, 'Alexander',   'Volkanovski',  'avolkanovski@ufc.com',  '012345 678910', '',          'active'),
(NULL, 'Khabib',      'Nurmagomedov', 'knurmagomedov@ufc.com', '012345 678910', '',          'active'),
(NULL, 'Kamaru',      'Usman',        'kusman@ufc.com',        '012345 678910', '',          'active'),
(NULL, 'Israel',      'Adesanya',     'iadesanya@ufc.com',     '012345 678910', '',          'active'),
(NULL, 'Henry',       'Cejudo',       'hcejudo@ufc.com',       '012345 678910', '',          'active'),
(NULL, 'Valentina',   'Shevchenko',   'vshevchenko@ufc.com',   '012345 678910', '',          'active'),
(NULL, 'Tyron',       'Woodley',      'twoodley@ufc.com',      '012345 678910', '',          'active'),
(NULL, 'Rose',        'Namajunas ',   'rnamajunas@ufc.com',    '012345 678910', '',          'active'),
(NULL, 'Tony',        'Ferguson ',    'tferguson@ufc.com',     '012345 678910', '',          'active'),
(NULL, 'Jorge',       'Masvidal ',    'jmasvidal@ufc.com',     '012345 678910', '',          'active'),
(NULL, 'Nate',        'Diaz ',        'ndiaz@ufc.com',         '012345 678910', '',          'active'),
(NULL, 'Conor',       'McGregor ',    'cmcGregor@ufc.com',     '012345 678910', '',          'active'),
(NULL, 'Cris',        'Cyborg ',      'ccyborg@ufc.com',       '012345 678910', '',          'active'),
(NULL, 'Tecia',       'Torres ',      'ttorres@ufc.com',       '012345 678910', '',          'active'),
(NULL, 'Ronda',       'Rousey ',      'rrousey@ufc.com',       '012345 678910', '',          'active'),
(NULL, 'Holly',       'Holm ',        'hholm@ufc.com',         '012345 678910', '',          'active'),
(NULL, 'Joanna',      'Jedrzejczyk ', 'jjedrzejczyk@ufc.com',  '012345 678910', '',          'active');
```

![Application Migration Service](/images/3/00020.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

8. Sử dụng lệnh SELECT để hiển thị bảng:

```
SELECT * FROM user;
```

- Sử dụng exit để rời khỏi.

![Application Migration Service](/images/3/00021.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

