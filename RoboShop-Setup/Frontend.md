# Frontend

The frontend is the service in RobotShop to serve the web content over Nginx.

To Install Nginx.

```
# yum install nginx -y
# systemctl enable nginx 
# systemctl start nginx 
```

Let's download the HTDOCS content and deploy under the Nginx path.

```
# curl -s -L -o /tmp/frontend.zip "https://dev.azure.com/DevOps-Batches/f4b641c1-99db-46d1-8110-5c6c24ce2fb9/_apis/git/repositories/a781da9c-8fca-4605-8928-53c962282b74/items?path=%2F&versionDescriptor%5BversionOptions%5D=0&versionDescriptor%5BversionType%5D=0&versionDescriptor%5Bversion%5D=master&resolveLfs=true&%24format=zip&api-version=5.0&download=true"
```

Deploy in Nginx Default Location.

```
# cd /usr/share/nginx/html
# rm -rf * 
# unzip /tmp/frontend.zip
# mv static/* .
# rm -rf static README.md
# mv localhost.conf /etc/nginx/default.d/roboshop.conf
```

Finally restart the service once to effect the changes.

```
# systemctl restart nginx 
```