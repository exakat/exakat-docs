.. _php-useobjectapi:

.. _use-php-object-api:

Use PHP Object API
++++++++++++++++++

  OOP API is the modern version of the PHP API.

When PHP offers the alternative between procedural and OOP api for the same features, it is recommended to use the OOP API. 

Often, this least to more compact code, as methods are shorter, and there is no need to bring the resource around. Lots of new extensions are directly written in OOP form too.

OOP / procedural alternatives are available for `mysqli <https://www.php.net/manual/en/book.`mysqli <https://www.php.net/mysqli>`_.php>`_, `tidy <https://www.php.net/manual/en/book.`tidy <https://www.php.net/tidy>`_.php>`_, `cairo <https://www.php.net/manual/en/book.cairo.php>`_, `finfo <https://www.php.net/manual/en/book.fileinfo.php>`_, and some others.

.. code-block:: php
   
   <?php
   /// OOP version
   $mysqli = new mysqli("localhost", "my_user", "my_password", "world");
   
   /* check connection */
   if ($mysqli->connect_errno) {
       printf("Connect failed: %s\n", $mysqli->connect_error);
       exit();
   }
   
   /* Create table doesn't return a resultset */
   if ($mysqli->query("CREATE TEMPORARY TABLE myCity LIKE City") === TRUE) {
       printf("Table myCity successfully created.\n");
   }
   
   /* Select queries return a resultset */
   if ($result = $mysqli->query("SELECT Name FROM City LIMIT 10")) {
       printf("Select returned %d rows.\n", $result->num_rows);
   
       /* free result set */
       $result->close();
   }
   ?>

Suggestions
___________

* Use the object API




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseObjectApi                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | object-api                                                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `use-object-api <https://github.com/dseguy/clearPHP/tree/master/rules/use-object-api.md>`__                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-php-useobjectapi`, :ref:`case-prestashop-php-useobjectapi`                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


