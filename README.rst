Django-PostgresPool
===================

This is a simple Postgres Connection Pooling backend for Django 1.4+, powered by the lovely and beautiful SQLAlchemy.


Usage
-----

Using Django-PostgresPool is simple, just set ``django_postgrespool`` as your connection engine:

::

    DATABASES = {
        'default': {
            'ENGINE': 'django_postgrespool'


If you're using the `dj-database-url <https://crate.io/packages/dj-database-url/>`_ module:

::

    import dj_database_url

    DATABASES['default'] = dj_database_url.config()
    DATABASES['default']['ENGINE'] = 'django_postgrespool'

If you're using `south <http://south.aeracode.org>`_:

::

    SOUTH_DATABASE_ADAPTERS = {
        'default': 'south.db.postgresql_psycopg2'
    }


Everything should work as expected.


Installation
------------

Installing Django-PostgresPool is simple, with pip::

    $ pip install django-postgrespool

Configuration
-------------

Optionally, you can provide additional options to pass to SQLAlchemy's pool creation::

    DATABASE_POOL_ARGS = {
        'max_overflow': 10,
        'pool_size': 5,
        'recycle': 300
    }

Django 1.3 Support
------------------

django-postgrespool currently supports Django 1.4 and greater. See `this ticket <https://github.com/kennethreitz/django-postgrespool/pull/9>`_ for 1.3 support.