.. _performances-fetchonerowformat:

.. _fetch-one-row-format:

Fetch One Row Format
++++++++++++++++++++

  When reading results with ext/`Sqlite3 <https://www.php.net/sqlite3>`_, it is recommended to explicitly request ``SQLITE3_NUM`` or ``SQLITE3_ASSOC``, while avoiding the default value and ``SQLITE3_BOTH``.


.. code-block:: php
   
   <?php
   
   $res = $database->query($query);
   
   // Fastest version, but less readable
   $row = $res->fetchArray(\SQLITE3_NUM);
   // Almost the fastest version, and more readable
   $row = $res->fetchArray(\SQLITE3_ASSOC);
   
   // Default version. Quite slow
   $row = $res->fetchArray();
   
   // Worse case
   $row = $res->fetchArray(\SQLITE3_BOTH);
   
   ?>


This is a micro-optimisation. The difference may be visible with 200k rows fetches, and measurable with 10k.

Suggestions
___________

* Specify the result format when reading rows from a Sqlite3 database




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/FetchOneRowFormat                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Performances <ruleset-Performances>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | csv                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


