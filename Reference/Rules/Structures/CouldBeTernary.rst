.. _structures-couldbeternary:

.. _could-be-ternary:

Could Be Ternary
++++++++++++++++

  This control structure may be replaced by a ternary operator. 

Th ternary operator may be shorter and easier to read than the full blown if-then-else structure. 
Depending on the situation, the null-ternary and the coalesce operator may also be a good alternative.

.. code-block:: php
   
   <?php
   
   // original structure
   if (empty($a)) {
       $b = 1;
   } else {
       $b = foo();
   }
   
   // ternary version : 
   $b = empty($a) ? 1 : foo();
   
   ?>

See also PHP Shorthand If/Else Using Ternary Operators (?:) `<https://davidwalsh.name/php-shorthand-if-else-ternary-operators>`_ and Shorthand comparisons in PHP `<https://stitcher.io/blog/shorthand-comparisons-in-php>`_.


Suggestions
___________

* Update the syntax to use the ternary operator




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CouldBeTernary                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | ternary, coalesce, null-ternary, short-assignation                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


