Deployment
==========

Installations
*************



* Install LAMP 
* Install composer 
* Install git
* Clone the KHRO ::
 cd / var/www
 git clone git@gitlab .com: khro /khro - backend . git
 cd khro - backend




**Set Permissions** ::

 sudo chgrp www - data ../ khro - backend ;
 sudo chown -R <username >: www - data ../ khro - backend /;
 sudo chmod -R 775 ../ khro - backend / storage /;
 sudo chmod -R 775 ../ khro - backend / bootstrap / cache ;
 sudo chmod g+s ../ khro - backend ;


**Install laravel dependencies (takes a while)** ::

    composer update

**Configurations** ::

#. Setup virtual host 3
Create to /etc/apache2/sites-available/khro.conf: ::

     sudo cp /etc/ apache2 /sites - available /000 - default . conf / etc/ apache2 /
 sites - available / khro . conf ;

#. Open to /etc/apache2/sites-available/khro.conf: ::

 sudo subl /etc/ apache2 /sites - available / khro . conf ;
	 php artisan passport:install

#. Add to /etc/apache2/sites-available/khro.conf: ::

	ServerName khro
 DocumentRoot /var/www/khro - backend / public
 <Directory "/var/www/khro - backend / public ">
 AllowOverride All
 </ Directory >

#. Open to /etc/hosts
sudo subl /etc/hosts
Add to /etc/hosts: ::

	127.0.0.1 khro

#. Activate the VH
: ::

	sudo a2ensite khro . conf && sudo service apache2 restart ;
#. Visit the Virtual Host
http://khro
Set up DB
copy and edit accordingly : ::
 cp . env. example .env && subl . env


Migration
*******

Populate DB ::
 cd ˜ && mysql -u <username > -p -e " CREATE DATABASE
 khro_master_warehouse ;" && mysql -u <username > -p
 khro_master_warehouse < khro_master_warehouse . sql && cd / var/ www/
 khro_backend && php artisan migrate



Backup
******

Create cronjob to run backup script, having edited and moved the backup script to home
directory, use crontab to add ::


 0 0 1 * * ./ home / user / db_backup .sh


Loading data from KHRO Microservice to KHRO Warehouse
*****************************************************
::

 cd / var / www/khro - backend && php artisn dhismicroservicepull { - - period =}
 { - - indicator =} { - - location =}




