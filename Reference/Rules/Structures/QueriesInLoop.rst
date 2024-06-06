.. _structures-queriesinloop:

.. _queries-in-loops:

Queries In Loops
++++++++++++++++

  Avoid querying databases in a loop. 

Querying an external database in a loop usually leads to performances problems. This is also called the 'n + 1 problem'. 

This problem applies also to prepared statement : when such statement are called in a loop, they are slower than one-time large queries.

It is recommended to reduce the number of queries by making one query, and dispatching the results afterwards. This is true with SQL databases, graph queries, LDAP queries, etc. 
This optimisation is not always possible : for example, some SQL queries may not be prepared, like ``DROP TABLE`` or ``DESC``. ``UPDATE`` commands often update one row at a time, and grouping such queries may be counter-productive or unsafe. 

This analysis looks for query calls inside loops, and within one functioncall.

.. code-block:: php
   
   <?php
   
   // Typical N = 1 problem : there will be as many queries as there are elements in $array
   $ids = array(1,2,3,5,6,10);
   
   $db = new SQLite3('mysqlitedb.db');
   
   // all the IDS are merged into the query at once
   $results = $db->query('SELECT bar FROM foo WHERE id  in ('.implode(',', $id).')');
   while ($row = $results->fetchArray()) {
       var_dump($row);
   }
   
   
   // Typical N = 1 problem : there will be as many queries as there are elements in $array
   $ids = array(1,2,3,5,6,10);
   
   $db = new SQLite3('mysqlitedb.db');
   
   foreach($ids as $id) {
       $results = $db->query('SELECT bar FROM foo WHERE id = '.$id);
       while ($row = $results->fetchArray()) {
           var_dump($row);
       }
   }
   
   ?>

See also `E N+1 PROBLEM IN ORMS SOLVING THE N+1 PROBLEM IN ORMS <https://thecodingmachine.io/solving-n-plus-1-problem-in-orms>`_.


Suggestions
___________

* Batch calls by using WHERE clauses and applying the same operation to all similar data
* Use native commands to avoid double query : REPLACE instead of SELECT-(UPDATE/INSERT), or UPSERT, for example




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/QueriesInLoop                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | query, loop                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-teampass-structures-queriesinloop`, :ref:`case-openemr-structures-queriesinloop`                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+


