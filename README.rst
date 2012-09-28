Django-PostgresPool
===================

This is a simple Postgres Connection Pooling backend for Django, powered by the lovely and beautiful SQLAlchemy.

**Experimental**: use with caution.


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