django-postgrespool
===================

This is an elegant Postgres Connection Pool backend for Django. Use with caution.

It's powered by the lovely and beautiful SQLAlchemy.


Usage
-----

Using Django-PostgresPool is simple, just set ``django_postgrespool`` as your connection engine:

::
    DATABASES = {
        'default': {
            'ENGINE': 'django_postgrespool'
    ...

If you're using the `dj-database-url <https://crate.io/packages/dj-database-url/>`_ module::

    import dj_database_url

    DATABASES['default'] = dj_database_url.config()
    DATABASES['default']['ENGINE'] = 'django_postgrespool'

Everything should work as expected.


Installation
-----------

Installing Django-PostgresPool is simple, with pip::

    $ pip install django-postgrespool