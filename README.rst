
TUNGSTEN DASHBOARD
==================

Tungsten Dashboard is open source client interface with dashboard for Tungsten Fabric.
More information about Tungsten Fabric You can find:

https://github.com/tungstenfabric/website

Project actual status is development stage, work only in development environment

Tungesten Dasboard use APACHE LICENSE, for more info check LICENSE

HOW TO INSTALL
--------------

Add repo:

.. code::

   sudo add-apt-repository ppa:deadsnakes/ppa
   sudo apt-get update

Install/check installation of python 3.6/venv:

.. code::

   sudo apt-get install python3.6
   sudo apt install python3.6-venv

Install/check installation of Docker:

.. code::

   sudo apt-get install docker.io

Clone project repo from github:

.. code::

   git clone git@github.com:tungstenfabric/tungsten-ci-dashboard.git
   cd tungsten-ci-dashboard/

Set venv with dependencies for project:

.. code::

   python3.6 -m venv .venv
   source .venv/bin/activate
   pip install setuptools wheel
   make install-dev

For develop purpose set db in docker:

.. code::

   docker run --name zuul_db -e MYSQL_ROOT_PASSWORD=root -p 3306:3306 -d mariadb:latest
   mysql -u root -pmysqlpass < zuul.sql

File **zuul.sql** You should find in project repo

Deactivate venv:

.. code::

   deactivate

HOW TO DEPLOY IN DEVELOPMENT ENV
--------------------------------

Enter to Tungsten Dashboard directory

.. code::

   cd [dir_with_file]

Activate venv:

.. code::

   source ./venv/bin/activate
   `

Run

.. code::

   make serve

**You will get application working on localhost:3000
Debugger in on**

HOW TO RUN TEST
---------------

Enter to Tungsten Dashboard directory

.. code::

   cd [dir_with_file]

Run tests

.. code::

   make test

**All tests You can find in /tests**
