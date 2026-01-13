.. _extensions-extsqlsrv:

.. _ext-sqlsrv:

ext/sqlsrv
++++++++++

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


