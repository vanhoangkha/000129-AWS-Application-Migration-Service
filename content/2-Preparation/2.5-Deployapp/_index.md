---
title : "Deploying an application"
date :  "`r Sys.Date()`" 
weight : 5
chapter : false
pre : " <b> 2.5 </b> "
---

#### Deploying an application

1. Deploy the application. Perform the clone of the application code repository.

```
git clone https://github.com/First-Cloud-Journey/000004-EC2.git
```

![Application Migration Service](/images/3/00022.png?featherlight=false&width=90pc)

2. Go to the directory of lab 000004-EC2:

```
cd 000004-EC2
```
After successfully connecting to the EC2 instance, you will perform the following steps to prepare for deploying your application:

- Install Node.js on the EC2 instance.

- Install Node Version Manager (nvm) by entering the following content into the command line:

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash
```
Activate nvm by entering the following content into the command line:

```
nvm install 16
```
Check if Node.js has been installed successfully:

```
node -v
npm -v
```
![Application Migration Service](/images/3/00023.png?featherlight=false&width=90pc)

3. NPM stands for Node package manager and is a tool for creating and managing Javascript programming libraries for Node.js. Using npm init to initialize a project will create a sample package.json file.

```
npm init
```
Next, we perform dependencies installation:

- express
- Dotenv
- express-handlebars
- body-parser
- mysql

```
npm install express dotenv express-handlebars body-parser mysql
```

![Application Migration Service](/images/3/00024.png?featherlight=false&width=90pc)

4. Create an environment file (.env) and use the vi command to edit it. Configure the database:

```
DB_HOST = 'localhost'
DB_NAME = 'awsfcjuser'
DB_USER = 'root'
DB_PASS = '123456789@Aws'
```

- Where DB_HOST is the endpoint of the DB instance.
- DB_NAME is the name of the database created in the DB instance.
- DB_USER is the name of the database user created in the DB instance.
- DB_PASS is the password of the database user created in the DB instance.

Restart the Express server. Use Nodemon to save time:

```
npm install --save-dev nodemon
```

![Application Migration Service](/images/3/00025.png?featherlight=false&width=90pc)

5. Starting local server

```
npm start
```
![Application Migration Service](/images/3/00026.png?featherlight=false&width=90pc)

6. Access the EC2 interface

   - Select Instances
   - Choose the instance hosting your application.
   - Copy the Public IPv4 address.
   - Use the Public IPv4 address and port 5000 to test the application in a browser.

```
<Public IPv4 address>:5000
```

Example: 3.91.32.39:5000

![Application Migration Service](/images/3/00027.png?featherlight=false&width=90pc)