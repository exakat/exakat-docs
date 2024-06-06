.. _structures-modernempty:

.. _modernize-empty-with-expression:

Modernize Empty With Expression
+++++++++++++++++++++++++++++++

  empty() accepts expressions as argument. This feature was added in PHP 5.5. 

There is no need to store the expression in a variable before testing, unless it is reused later.

.. code-block:: php
   
   <?php
   
   // PHP 5.5+ empty() usage
   if (empty(foo($b . $c))) {
       doSomethingWithoutA();
   }
   
   // Compatible empty() usage
   $a = foo($b . $c);
   if (empty($a)) {
       doSomethingWithoutA();
   }
   
   // $a2 is reused, storage is legit
   $a2 = strtolower($b . $c);
   if (empty($a2)) {
       doSomething();
   } else {
       echo $a2;
   }
   
   ?>

See also `empty() <https://www.php.net/empty>`_ and `empty() supports arbitrary expressions <https://www.php.net/manual/en/migration55.new-features.php#migration55.new-features.empty>`_.


Suggestions
___________

* Avoid the temporary variable, and use directly empty()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ModernEmpty                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.5 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | empty                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


