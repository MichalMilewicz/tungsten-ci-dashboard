TUNGSTEN DASHBOARD
==================

Awesome CI Dashboard is open source client interface for Zuul Gating system

More information about Zuul Gating system you can find at

https://zuul-ci.org/docs/zuul/

Project actual status is development stage, work only in development environment

Tungesten Dasboard use APACHE 2.0 LICENSE, for more info check LICENSE

HOW TO INSTALL
--------------

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
   make install-dev



RUN Awesome CI Dashboard
--------------------------------


.. code:: console

    $ source .venv/bin/activate
    $ make serve

Server will listen on http://127.0.0.1:3000/

RUN TESTS
---------------

Enter to Tungsten Dashboard directory

.. code:: console

    $ source .venv/bin/activate
    $ make test && make lint

