# Shipping Service.

Shipping service is responsible for finding the distance of the package to be shipped and calculate the price based on that. 

Shipping service is written in Java, Hence we need to install Java.

1. Install Maven, This will install Java too 

```
# yum install maven -y
```

2. As per the standard process, we always run the applications as a normal user.

Create a user 

```
# useradd roboshop
```

3. Download the repo 

```
$ cd /home/roboshop
$ curl -s -L -o /tmp/shipping.zip "https://dev.azure.com/DevOps-Batches/f4b641c1-99db-46d1-8110-5c6c24ce2fb9/_apis/git/repositories/1ebc164b-f649-49b5-807d-2e55dc14628e/items?path=%2F&versionDescriptor%5BversionOptions%5D=0&versionDescriptor%5BversionType%5D=0&versionDescriptor%5Bversion%5D=master&resolveLfs=true&%24format=zip&api-version=5.0&download=true"
$ mkdir shipping
$ cd shipping
$ unzip /tmp/shipping.zip
$ mvn clean package 
$ mv target/shipping-1.0.jar shipping.jar 
```


4. Copy the service file and start the service.

```
# cp /home/roboshop/shipping/systemd.service /etc/systemd/system/shipping.service
# systemctl daemon-reload
# systemctl start shipping 
# systemctl enable shipping
```

