pgbackup
========

CLI for backing up remote PostgreSQL databases locally or to AWS S3.

Preparing for Development
-------------------------

1. Ensure ''pip'' and ''pipenv'' are installed.
2. Clone repository: ''git clone git@github.com:JJayJungleJim/pgbackup''
3. Fetch development dependencies: ''make install''

Usage
-----

Pass in a full database URL, the storage driver, and destination.

S3 Example w/ bucket name:

::

    $ pgbackup postgres://bob@example.com:5432/db_one --driver s3 backups

Local example w/ local path:

::

    $ pgbackup postgres://bob@example.com:5432/db_one --driver local /var/local/db_one/backups/dump.sql

Running Tests
-------------

Run test locally using ''make'' if virtualenv is active:

::

    $ make 

If virtualenv isn't active then use:

::

    $ pipenv run make

