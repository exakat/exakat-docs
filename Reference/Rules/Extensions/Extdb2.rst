.. _extensions-extdb2:


.. _ext-db2:

ext/db2
+++++++


.. meta::

	:description:

		ext/db2: Extension for IBM DB2, Cloudscape and Apache Derby.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: ext/db2

	:twitter:description: ext/db2: Extension for IBM DB2, Cloudscape and Apache Derby

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: ext/db2

	:og:type: article

	:og:description: Extension for IBM DB2, Cloudscape and Apache Derby

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/db2.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extdb2.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extdb2.html","name":"ext\/db2","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension for IBM DB2, Cloudscape and Apache Derby","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/db2.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

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
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
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


