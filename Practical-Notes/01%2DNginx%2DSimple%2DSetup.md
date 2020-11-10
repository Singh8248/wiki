# Install Nginx Web Server 

```
$ sudo yum install nginx -y 
$ sudo systemctl enable nginx 
$ sudo systemctl start nginx 
```

Access your web server

# Configure our own web-site

```
$ cd /usr/share/nginx/html
$ sudo rm -rf * 
$ sudo curl https://github.com/cloudacademy/static-website-example/archive/master.zip -O -L
$ sudo unzip master.zip
$ sudo mv static-website-example-master/* .
```

Now you can access the hosted website.

