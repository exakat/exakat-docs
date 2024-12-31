.. _type-sql:

.. _sql-queries:

SQL queries
+++++++++++

.. meta\:\:
	:description:
		SQL queries: SQL queries, detected in literal strings.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: SQL queries
	:twitter:description: SQL queries: SQL queries, detected in literal strings
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: SQL queries
	:og:type: article
	:og:description: SQL queries, detected in literal strings
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Type/Sql.html
	:og:locale: en
  SQL queries, detected in literal strings. 

SQL queries are detected with keywords, inside literals or concatenations.

.. code-block:: php
   
   <?php
   
   // SQL in a string
   $query = 'SELECT name FROM users WHERE id = 1';
   
   // SQL in a concatenation
   $query = 'SELECT name FROM '.$table_users.' WHERE id = 1';
   
   // SQL in a Heredoc
   $query = <<<SQL
   SELECT name FROM $table_users WHERE id = 1
   SQL;
   
   ?>

Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/Sql                                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Inventory <ruleset-Inventory>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.1                                                                                                                                                                                  |
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


