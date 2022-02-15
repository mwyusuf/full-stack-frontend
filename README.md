# full-stack-frontend

## Introduction
### What is Fullstack
Someone who can build an application from start to finish, including front end and backend.

## Understanding the Internet
It works by using a packet routing network that follows Internet Protocol (IP) and Transport Control Protocol (TCP) [5]. TCP and IP work together to ensure that data transmission across the internet is consistent and reliable, no matter which device you're using or where you're using it. Basically a series of system globally interconnected devices. Not to be confused with intranet, which basically internet but private.

## Servers
It serves content and also respond request, it serves something back.

```sh
yusuf@Yusufs-MacBook-Pro full-stack-frontend % node simpleServer.js 
Server started! listening on port 8080
```
<img width="258" alt="image" src="https://user-images.githubusercontent.com/85268263/153993623-9c5ce85d-b7bd-40f6-bb6b-54a048664f27.png">

## SSH
The Secure Shell Protocol is a cryptographic network protocol for operating network services securely over an unsecured network. Its most notable applications are remote login and command-line execution. SSH applications are based on a client–server architecture, connecting an SSH client instance with an SSH server.

```sh
yusuf@Yusufs-MacBook-Pro .ssh % ls
id_rsa		id_rsa.pub	known_hosts
yusuf@Yusufs-MacBook-Pro .ssh % vim id_rsa
yusuf@Yusufs-MacBook-Pro .ssh % vim id_rsa.pub
```

## Nginx
Nginx
Nginx, stylized as NGINX, nginx or NginX, is a web server that can also be used as a reverse proxy, load balancer, mail proxy and HTTP cache. The software was created by Igor Sysoev and publicly released in 2004. Nginx is free and open-source software, released under the terms of the 2-clause BSD license. it can do or act as :
- Reverse proxy
- Web server
- Proxy server

Some of nginx command line :
Install nginx
```
$ sudo apt install nginx
```
Start nginx
```
$ sudo service nginx start
```
Show nginx configuration
```
$ sudo less /etc/nginx/sites-available/default
```
Create and edit index.html
```
$ sudo vi /var/www/html/index.html
```
### Node.js
Node.js is an open-source, cross-platform, back-end JavaScript runtime environment that runs on the V8 engine and executes JavaScript code outside a web browser.

Install NodeJS and npm
```
$ sudo apt install nodejs npm
```
Install git
```
$ sudo apt install git
```
### Application Setup
Change ownership of the www directory to the current user
```
$ sudo chown -R $USER:$USER /var/www
```
Create application directory
```
$ mkdir /var/www/app
```
Move into app directory and initialize empty git repo
```
$ cd /var/www/app && git init
```
Create directories
```
$ mkdir -p ui/js ui/html ui/css
```
Create empty app file
```
$ touch app.js
```
Initialize project
```
$ npm init
```
install express
```
$ npm i express --save
```
edit app
```
$ vi app.js
```
Run application
```
$ node app.js
```

### Process Manager
a process manager is a way to :
- Keeps your application running
- Handles errors and restarts
- Handle logging and clustering

Install PM2
```
$ sudo npm i -g pm2
```
Start PM2
```
$ pm2 start app.js
```
Setup auto restart
```
$ pm2 save
$ pm2 startup
```