django-pgschemas
================

.. image:: https://img.shields.io/badge/packaging-poetry-purple.svg
    :alt: Packaging: poetry
    :target: https://python-poetry.org/

.. image:: https://github.com/lorinkoz/django-pgschemas/workflows/code/badge.svg
    :alt: Build status
    :target: https://github.com/lorinkoz/django-pgschemas/actions

.. image:: https://readthedocs.org/projects/django-pgschemas/badge/?version=latest
    :alt: Documentation status
    :target: https://django-pgschemas.readthedocs.io/

.. image:: https://coveralls.io/repos/github/lorinkoz/django-pgschemas/badge.svg?branch=master
    :alt: Code coverage
    :target: https://coveralls.io/github/lorinkoz/django-pgschemas?branch=master

.. image:: https://badge.fury.io/py/django-pgschemas.svg
    :alt: PyPi version
    :target: http://badge.fury.io/py/django-pgschemas

.. image:: https://pepy.tech/badge/django-pgschemas/month
    :alt: Downloads
    :target: https://pepy.tech/project/django-pgschemas/

|

This app uses Postgres schemas to support data multi-tenancy in a single
Django project. It is a fork of `django-tenants`_ with some conceptual changes:

- There are static tenants and dynamic tenants. Static tenants can have their
  own apps and urlconf.
- Tenants can be routed via: (1) URL using subdomain or subfolder on shared
  subdomain, (2) session or (3) headers.
- Public is no longer the schema for storing the main site data. Public is only
  used for shared data across all tenants. Table "overriding" via search path is
  not encouraged.
- Management commands can be run on multiple schemas via wildcards, either
  sequentially or in parallel using multithreading.

.. _django-tenants: https://github.com/django-tenants/django-tenants

Documentation
-------------

https://django-pgschemas.readthedocs.io/

Contributing
------------

- Join the discussion at https://github.com/lorinkoz/django-pgschemas/discussions.
- PRs are welcome! If you have questions or comments, please use the discussions
  link above.
- To run the test suite run ``make`` or ``make coverage``. The tests for this
  project live inside a small django project called ``sandbox``.

Credits
-------

* Tom Turner for `django-tenants`_.
* Bernardo Pires for `django-tenant-schemas`_.

.. _django-tenants: https://github.com/django-tenants/django-tenants
.. _django-tenant-schemas: https://github.com/bernardopires/django-tenant-schemas
