.. _structures-toomanychainedcalls:

.. _too-many-chained-calls:

Too Many Chained Calls
++++++++++++++++++++++

  Report chained calls of functions, methods and `static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods are crammed in one expression.

This makes the whole expression difficult to read, and it is possible to miss some important parameter or intermidate calls when reviewing it. 

This may lead to bugs when some of the intermediate calls may return an invalid `result <https://www.php.net/result>`_, such as `null` or `false` in case of `error <https://www.php.net/error>`_. Those must be tested before being propagated.

.. code-block:: php
   
   <?php
   
   // 
   $s = strtoupper(hash('whirlpool',hash('sha1', microtime(true).crypt(uniqid(rand(), true)))));
   
   ?>

Suggestions
___________

* Reduce the number of needed calls in the expression
* Add intermediate checks on the values
* Split the expression on multiple lines, and add a comment with a summary first




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/TooManyChainedCalls                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


