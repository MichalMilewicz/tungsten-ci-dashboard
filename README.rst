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

.. code:: console

   $ sudo apt install python3.6 python3.6-venv

Set venv with dependencies for project:

.. code:: console

   $ python3.6 -m venv .venv
   $ source .venv/bin/activate
   $ pip install setuptools wheel
   $ make install-dev

Run vagrant for remote services like Zuul and Gerrit for development purposes.

.. code:: console

    $ make dev-run


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

