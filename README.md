# docker-nginx-fpm-mysql

You need docker and docker-compose set up and running before.

This is just an example to setup a development pipeline using 3 containers:
 - nginx
 - php-fpm
 - mysql

You will have a data/www directory where you can put any php code.
The database will be stored persistantly in data/db.

Below you will find how to put a wordpress in it as example.

    git clone https://github.com/kykoonn/docker-nginx-fpm-mysql.git 
    cd docker-nginx-fpm-mysql
    docker-compose build
    docker-compose up

At this point you will have an empty server, so put some stuff in data/www:

    curl -s https://wordpress.org/latest.tar.gz|tar xzf - -C data/www

Browse to your docker host: http://$DOCKER_HOST_IP/wordpress and finish the wordpress setup.
