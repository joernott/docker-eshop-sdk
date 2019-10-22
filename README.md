# Development base

Docker based local development environment 

## What we have here

For the start:

* Apache 2.4 
* PHP 7.3 fpm with xDebug, remote debuggind and error reporting enabled
* MySQL 5.7 with adminer
* Npm

## Quick start

```
git clone https://github.com/Sieg/development.git myProjectName
cd myProjectName

./build.sh
docker-compose up --build -d
```

Access the website through the http://localhost

Adminer is available via http://localhost:8080

## Running php stuff

Call commands directly on the container:
```
docker-compose run php php -v
```

Login to the container, and run the commands from inside:
```
docker-compose exec php bash
php -v
```

## Running npm commands

```
docker-compose run node npm install bootstrap
```