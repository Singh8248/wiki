# Payment Service 

This service is responsible for payments in RoboShop e-commerce app.

This service is written on `Python 3`, So need it to run this app.

CentOS 7 comes with `Python 2` by default. So we need `Python 3` to be installed.

1. Install Python 3

```
# yum install python36 gcc python3-devel -y
```

2. Create a user for running the application 

```
# useradd roboshop
```

3. Download the repo.

```
$ cd /home/roboshop
$ curl -L -s -o /tmp/payment.zip "https://dev.azure.com/DevOps-Batches/f4b641c1-99db-46d1-8110-5c6c24ce2fb9/_apis/git/repositories/64e9a902-e729-44ad-a562-8f605ae9617e/items?path=%2F&versionDescriptor%5BversionOptions%5D=0&versionDescriptor%5BversionType%5D=0&versionDescriptor%5Bversion%5D=master&resolveLfs=true&%24format=zip&api-version=5.0&download=true"
$ mkdir payment
$ cd payment
$ unzip /tmp/payment.zip
```

4. Install the dependencies

```
# cd /home/roboshop/payment 
# pip3 install -r requirements.txt
```

**Note: Above command may fail with permission denied, So run as root user**

5. Update the roboshop user and group id in `payment.ini` file.

6. Setup the service 

```
# mv /home/roboshop/payment/systemd.service /etc/systemd/system/payment.service
# systemctl daemon-reload
# systemctl enable payment 
# systemctl start payment
```
