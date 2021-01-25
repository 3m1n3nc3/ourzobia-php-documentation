*******************
Server Requirements
*******************

`PHP <https://www.php.net/>`_ version 7.2 or newer is required, with the
`*intl* extension <https://www.php.net/manual/en/intl.requirements.php>`_, `*gd* extension <https://www.php.net/manual/en/image.requirements.php>`_ and `*mbstring* extension <https://www.php.net/manual/en/mbstring.requirements.php>`_
installed.

You should also have the following PHP extensions enabled on your server:

  - ``php-json`` 
  - ``php-mysqli``
  - ``php-curl``
  - ``php-zip``
  - ``php-xml``
  - ``php-gd``
  - ``php-mbstring``
  - ``php-intl``

You also have to set ``allow_url_fopen`` to ``1`` in your php.ini directive.

In order to use :doc:`Automation <../system/crone>` and also be able to receive automatic security updates, you will need access to Cron Jobs on your Hosting Server.

A database is the most important required for working with Ourzobia PHP - Social Peer to Peer Donation System, the system has been pre-configured to work flawlessly with MySQL (5.1+). But because of the flexibility of the Codeigniter framework other Databases can also be configured to work with Ourzobia PHP - Social Peer to Peer Donation System, although you would have to manually reconfigure the system to work with your alternative database.

Currently supported databases are:

  - MySQL (5.1+) via the *MySQLi* driver
  - PostgreSQL via the *Postgre* driver
  - SQLite3 via the *SQLite3* driver 

Set the permissions of the following files and directories to ``755``:

  - ``writable/session Writable``
  - ``writable/updates Writable``
  - ``public/sitemap Writable``
  - ``public/uploads Writable``
  - ``app/Controllers/Install``

.. toctree::
    :glob:
    :titlesonly: