# User Service

This service is responsible for User Logins and Registrations Service in RobotShop e-commerce portal.

This service is written in NodeJS, Hence need to install NodeJS in the system.


```
# yum install nodejs make gcc-c++ -y 
```

Let's now set up the User application.

As part of operating system standards, we run all the applications and databases as a normal user but not with root user.

So to run the User service we choose to run as a normal user and that user name should be more relevant to the project. Hence we will use `roboshop` as the username to run the service.

```
# useradd roboshop
```

So let's switch to the `roboshop` user and run the following commands.

```
$ curl -s -L -o /tmp/user.zip "https://dev.azure.com/DevOps-Batches/f4b641c1-99db-46d1-8110-5c6c24ce2fb9/_apis/git/repositories/360c1f78-e8ed-41e8-8b3d-bdd12dc8a6a1/items?path=%2F&versionDescriptor%5BversionOptions%5D=0&versionDescriptor%5BversionType%5D=0&versionDescriptor%5Bversion%5D=master&resolveLfs=true&%24format=zip&api-version=5.0&download=true"
$ cd /home/roboshop
$ mkdir user
$ cd user
$ unzip /tmp/user.zip
$ npm install 
```


Now, lets set up the service with systemctl.

```
# mv /home/roboshop/user/systemd.service /etc/systemd/system/user.service
# systemctl daemon-reload
# systemctl start user
# systemctl enable user
```


