Deployment
==========

Installations
*************

To run this package you need Python 3.5.2+, PostgresSQL and Redis.

* Install Python 3.5.2+ 
* Install PostgresSQL 
* Install git
* Install Redis

This installation method assumes you are the author of the Rootshelf HGSF application and wish to develop it. Below are instructions to to install the package to a Python virtual environment using pip command in an editable mode.

**Installation** ::

	cd mfarm.rootshelf  # This is the folder with setup.py file
	python3 -m venv env  # Create virtual environment
	source env/bin/activate  # Activate virtual environment
	pip install -U pip  # Make sure pip itself is up-to-date
	pip install -r requirements.txt  # Install this package

Running the website
*******************

**Create the database:** ::

   psql create rootshelf_dev  # Create database

Note
****

Edit the mfarm/rootshelf/conf/development.ini file and change the connection string to the one used on your environment. i.e.: postgresql://username:passwd@localhost/rootshelf_dev

**Sync models from this application to the newly created database:** ::

	ws-alembic -c mfarm/rootshelf/conf/development.ini -x packages=all revision --auto -m "Initial migration"
	ws-alembic -c mfarm/rootshelf/conf/development.ini -x packages=all upgrade head
	ws-sync-db ws://mfarm/rootshelf/conf/development.ini


**Add a user with administrative rights:** ::

	ws-create-custom-user ws://mfarm/rootshelf/conf/development.ini admin@example.com mypassword

**Start the application:** ::

	pserve ws://mfarm/rootshelf/conf/development.ini





