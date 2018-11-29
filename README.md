# docker-wordpress-dev

A docker build for local wordpress development.

Nginx, MariaDB, PHP-7.2-FPM with FastCgi cache

## Requirements

Docker
Docker Compose

## Install

Clone the repository to a directory
```
git clone https://github.com/eric-mathison/docker-wordpress-dev.git
```

Once the repo is cloned, create required directories for the project.
```
mkdir logs/nginx
mkdir cache/
mkdir mysql/
mkdir wordpress/
```

Next, open `wordpress.conf` in an editor and change the domain.
```
server_name dev.localhost;    // change or leave as is
```

Add entry in host file
*Chrome automatically will redirect .localhost to 127.0.0.1*
```
127.0.0.1 dev.localhost
```

## Usage

When you are ready to create the containers, use docker-compose up.
```
docker-compose up -d
```

If you did not change the server_name, the new wordrpess installation will be accessible at `http://dev.localhost`

