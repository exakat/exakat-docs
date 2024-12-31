.. _extensions-extmssql:

.. _ext-mssql:

ext/mssql
+++++++++

.. meta\:\:
	:description:
		ext/mssql: Extension MSSQL, Microsoft SQL Server.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/mssql
	:twitter:description: ext/mssql: Extension MSSQL, Microsoft SQL Server
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/mssql
	:og:type: article
	:og:description: Extension MSSQL, Microsoft SQL Server
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extmssql.html
	:og:locale: en
  Extension MSSQL, Microsoft SQL Server.

These functions allow you to access MS SQL Server database.

.. code-block:: php
   
   <?php
   // Connect to MSSQL
   $link = mssql_connect('KALLESPC\SQLEXPRESS', 'sa', 'phpfi');
   
   if (!$link || !mssql_select_db('php', $link)) {
       die('Unable to connect or select database!');
   }
   
   // Do a simple query, select the version of 
   // MSSQL and print it.
   $version = mssql_query('SELECT @@VERSION');
   $row = mssql_fetch_array($version);
   
   echo $row[0];
   
   // Clean up
   mssql_free_result($version);
   ?>

See also `Microsoft SQL Server <http://www.php.net/manual/en/book.mssql.php>`_ and `Microsoft PHP Driver for SQL Server <https://docs.microsoft.com/en-us/sql/connect/php/microsoft-php-driver-for-sql-server>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extmssql                                                                                                                                                                     |
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


