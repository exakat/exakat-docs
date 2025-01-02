.. _extensions-extmysql:

.. _ext-mysql:

ext/mysql
+++++++++

.. meta::
	:description:
		ext/mysql: Extension for MySQL (Original MySQL API).
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/mysql
	:twitter:description: ext/mysql: Extension for MySQL (Original MySQL API)
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/mysql
	:og:type: article
	:og:description: Extension for MySQL (Original MySQL API)
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/mysql.html
	:og:locale: en
Extension for MySQL (Original MySQL API).

This extension is deprecated as of PHP 5.5.0, and has been removed as of PHP 7.0.0. Instead, either the `mysqli <https://www.php.net/mysqli>`_ or PDO_MySQL extension should be used. 

See also the MySQL API Overview for further help while choosing a MySQL API.

.. code-block:: php
   
   <?php
   $result = mysql_query('SELECT * WHERE 1=1');
   if (!$result) {
       die('Invalid query: ' . mysql_error());
   }
   
   ?>

See also `Original MySQL API <http://www.php.net/manual/en/book.mysql.php>`_ and `MySQL <http://www.mysql.com/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extmysql                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and older                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


