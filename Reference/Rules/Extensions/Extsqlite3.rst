.. _extensions-extsqlite3:

.. _ext-sqlite3:

ext/sqlite3
+++++++++++

.. meta::
	:description:
		ext/sqlite3: Extension Sqlite3.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/sqlite3
	:twitter:description: ext/sqlite3: Extension Sqlite3
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/sqlite3
	:og:type: article
	:og:description: Extension Sqlite3
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/sqlite3.html
	:og:locale: en
Extension `Sqlite3 <https://www.php.net/sqlite3>`_.

This extension adds support for SQLite version 3 databases. There used to be a Sqlite2 extension, which have been discontinued: this is the replacement.

.. code-block:: php
   
   <?php
   $db = new SQLite3('mysqlitedb.db');
   
   $results = $db->query('SELECT bar FROM foo');
   while ($row = $results->fetchArray()) {
       var_dump($row);
   }
   ?>

See also `ext/sqlite3 <https://www.php.net/manual/en/book.sqlite3.php>`_ and `Sqlite <http://sqlite.org/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extsqlite3                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


