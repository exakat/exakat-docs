.. _extensions-extsqlsrv:


.. _ext-sqlsrv:

ext/sqlsrv
++++++++++


.. meta::

	:description:

		ext/sqlsrv: Extension for Microsoft SQL Server Driver.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: ext/sqlsrv

	:twitter:description: ext/sqlsrv: Extension for Microsoft SQL Server Driver

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: ext/sqlsrv

	:og:type: article

	:og:description: Extension for Microsoft SQL Server Driver

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/sqlsrv.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extsqlsrv.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extsqlsrv.html","name":"ext\/sqlsrv","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension for Microsoft SQL Server Driver","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/sqlsrv.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension for Microsoft SQL Server Driver.

The SQLSRV extension allows you to access Microsoft SQL Server and SQL Azure databases when running PHP on Windows.

.. code-block:: php
   
   <?php
   $serverName = 'serverName\sqlexpress';
   $connectionInfo = array( 'Database'=>'dbName', 'UID'=>'username', 'PWD'=>'password' );
   $conn = sqlsrv_connect( $serverName, $connectionInfo);
   if( $conn === false ) {
        die( print_r( sqlsrv_errors(), true));
   }
   
   $sql = 'INSERT INTO Table_1 (id, data) VALUES (?, ?)';
   $params = array(1, 'some data');
   
   $stmt = sqlsrv_query( $conn, $sql, $params);
   if( $stmt === false ) {
        die( print_r( sqlsrv_errors(), true));
   }
   ?>

See also `Microsoft SQL Server Driver <https://www.php.net/sqlsrv>`_ and `PHP Driver for SQL Server Support for LocalDB <http://msdn.microsoft.com/en-us/library/hh487161.aspx>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extsqlsrv                                                                                                                                                                    |
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


