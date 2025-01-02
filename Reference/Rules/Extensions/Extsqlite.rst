.. _extensions-extsqlite:

.. _ext-sqlite:

ext/sqlite
++++++++++

.. meta::
	:description:
		ext/sqlite: Extension Sqlite 2.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/sqlite
	:twitter:description: ext/sqlite: Extension Sqlite 2
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/sqlite
	:og:type: article
	:og:description: Extension Sqlite 2
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/sqlite.html
	:og:locale: en
Extension Sqlite 2.

Support for SQLite version 2 databases. The support for this version of Sqlite has ended. It is recommended to use ``SQLite3``.

.. code-block:: php
   
   <?php
   
   if ($db = sqlite_open('mysqlitedb', 0666, $sqliteerror)) { 
       sqlite_query($db, 'CREATE TABLE foo (bar varchar(10))');
       sqlite_query($db, 'INSERT INTO foo VALUES ("fnord")');
       $result = sqlite_query($db, 'select bar from foo');
       var_dump(sqlite_fetch_array($result)); 
   } else {
       die($sqliteerror);
   }
   
   ?>

See also `ext/sqlite <https://www.php.net/manual/en/book.sqlite.php>`_ and `SQLite <http://sqlite.org/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extsqlite                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.3                                                                                                                                                                                  |
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


