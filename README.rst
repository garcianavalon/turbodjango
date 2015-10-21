***********
turbodjango
***********

.. contents::
   :local:
   :depth: 3


Vagrant box
===========

Up the box and login
::

    $vagrant up
    $vagrant ssh

Python deps

::
    $cd /vagrant
    $mk virtualenv your_project_venv_name
    $pip install -r requirements.txt

PostgreSQL Database

::
    $sudo su - postgres
    $createdb your_project_db_name
    $createuser -P django
    $psql
    postres=# GRANT ALL PRIVILEGES ON DATABASE your_project_db_name TO django;
    postres=# \q
    $exit

Migrations

:: 
    $python manage.py migrate

Run your website

::
    $python manage.py runserver 0.0.0.0:8000



