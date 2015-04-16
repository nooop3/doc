
.. _wp_install:

*****************
Install WordPress
*****************

Install AMP
===========

Install with Debian APT
-----------------------

For Debian distribution, 

Install and Setup XAMPP (Linux)
-------------------------------

Run the install::

  sudo ./xampp-linux-x64-5.6.3-0-installer.run

Defaut install path: ``/opt/lampp``

Check if the system default services is running::

  sudo service apache2 status
  sudo service mysql status

Stop system default Apache2 and mysql service::

  sudo service apache2 stop
  sudo service mysql stop

Two ways of controling the XAMPP services:

* GUI control: ``lampp/manager-linux-x64.run``
* Command line: ``lampp/xampp`` 

  run ``sudo ./xampp`` will show all functions.

Start XAMPP services::

  sudo xampp start

In browser open url: http://localhost/xampp/ for the homepage of XAMPP.

Setup the password for services::

  sudo ./xampp security

Copy ``wordpress/`` files to ``/lampp/htdocs``.

Create the database for WordPress
=================================

Default system mysql
--------------------

Enter mysql prompt::

  mysql -u root -p

type the password, then check the existed database in mysql prompt::

  SHOW DATABASES;

Build a mysql database for WordPress::

  CREATE DATABASE wpadmin;

Then::
  
  FLUSH PRIVILEGES;

With phpMyAdmin
---------------

Setup from Debian repository phpMyAdmin is easy::

  sudo apt-get install phpmyadmin

and include the web server settings in the configuration file: ``/etc/apache2/apache2.conf``::

  Include /etc/phpmyadmin/apache.conf

restart the web server, then open the link http://localhost/phpmyadmin/.

From 'Databases' card, enter new database name ``wpadmin``, press 'create'.

Setup WordPress
===============

Copy package ``

Change owner::
  
  sudo chown root:root -R wordpress/

Open url, http://localhost/wordpress/ to open setup page, press 'Let's go!', enter the database connection details::
  
  database name: wpadmin
  mysql user: root
  password: ******
  database host: localhost
  table prefix: wp_
  
For privilege problem, the following warned:

  Sorry, but I can’t write the ``wp-config.php`` file.

  You can create the ``wp-config.php`` manually and paste the following text into it.

and manually copy the text in the frame to build ``wordpress/wp-config.php``.

Press 'Run the install', then comes the welcome page.



