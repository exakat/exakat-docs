.. _structures-uselistwithforeach:

.. _use-list-with-foreach:

Use List With Foreach
+++++++++++++++++++++

  `Foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ structures accepts `list() <https://www.php.net/list>`_ as blind key. If the loop-value is an array with a fixed structure, it is possible to extract the values directly into variables with explicit names.

.. code-block:: php
   
   <?php
   
   // Short way to assign variables
   // Works on PHP 7.1, where list() accepts keys.
   foreach($names as list('first' => $first, 'last' => $last)) {
       doSomething($first, $last);
   }
   
   // Short way to assign variables
   // Works on all PHP versions with numerically indexed arrays.
   foreach($names as list($first, $last)) {
       doSomething($first, $last);
   }
   
   // Long way to assign variables
   foreach($names as $name) {
       $first = $name['first'];
       $last = $name['last'];
       
       doSomething($first, $last);
   }
   
   ?>

See also `list <https://www.php.net/manual/en/function.list.php>`_ and `foreach <https://www.php.net/manual/en/control-structures.foreach.php>`_.


Suggestions
___________

* Use the list keyword (or the short syntax), and simplify the array calls in the loop.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UseListWithForeach                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.4                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | class                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-mediawiki-structures-uselistwithforeach`                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


