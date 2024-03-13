.. _structures-couldcasttoarray:

.. _could-cast-to-array:

Could Cast To Array
+++++++++++++++++++

  The array cast operator transform a scalar into an array with that scalar. It also keeps an array as an array, so a single call to ``(array)`` is able to convert scalars to array, while keeping values already in array form intact.

.. code-block:: php
   
   <?php
   
   // 
   if (!is_array($a)) {
   	$a = [$a];
   }
   
   // equivalent to 
   $a = (array) $a;
   
   // same, with the else
   if (is_array($a)) {
   } else {
   	$a = array($a);
   }
   
   ?>

See also `Mastering the (array) Cast Operator in PHP <https://www.exakat.io/en/mastering-the-array-cast-operator-in-php-a-comprehensive-guide/>`_.


Suggestions
___________

* Use a direct cast to array




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CouldCastToArray                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | array, cast                                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


