.. _extensions-extdb2:

.. _ext-db2:

ext/db2
+++++++

  Extension for IBM DB2, Cloudscape and Apache Derby.

This extension gives access to IBM DB2 Universal Database, IBM Cloudscape, and Apache Derby databases using the DB2 Call Level Interface (DB2 CLI).


.. code-block:: php
   
   <?php
   $conn = db2_connect($database, $user, $password);
   
   if ($conn) {
       $stmt = db2_exec($conn, 'SELECT count(*) FROM animals');
       $res = db2_fetch_array( $stmt );
       echo $res[0] . PHP_EOL;
       
       // Turn AUTOCOMMIT off
       db2_autocommit($conn, DB2_AUTOCOMMIT_OFF);
      
       // Delete all rows from ANIMALS
       db2_exec($conn, 'DELETE FROM animals');
       
       $stmt = db2_exec($conn, 'SELECT count(*) FROM animals');
       $res = db2_fetch_array( $stmt );
       echo $res[0] . PHP_EOL;
       
       // Roll back the DELETE statement
       db2_rollback( $conn );
       
       $stmt = db2_exec( $conn, 'SELECT count(*) FROM animals' );
       $res = db2_fetch_array( $stmt );
       echo $res[0] . PHP_EOL;
       db2_close($conn);
   }
   ?>

See also `IBM Db2 <https://www.php.net/manual/en/book.ibm-db2.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extdb2                                                                                                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.8                                                                                                                                                                                   |
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


