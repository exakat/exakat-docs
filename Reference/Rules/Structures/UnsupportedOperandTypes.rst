.. _structures-unsupportedoperandtypes:

.. _unsupported-operand-types:

Unsupported Operand Types
+++++++++++++++++++++++++

  This `error <https://www.php.net/error>`_ is raised when trying to combine an array and a scalar value. 

Always checks that the types are compatible with the planned operations.


.. code-block:: php
   
   <?php
   
   const MY_ARRAY = 'error';
   
   // This leads to the infamous "Unsupported operand types" error
   $b = MY_ARRAY + array(3,4);
   
   ?>


PHP detects this `error <https://www.php.net/error>`_ at linting time, when using literal values. When `static <https://www.php.net/manual/en/language.oop5.static.php>`_ expression are involved, this `error <https://www.php.net/error>`_ will appear at execution time.

See also `PHP - Fatal error: Unsupported operand types [duplicate] <https://stackoverflow.com/questions/2108875/php-fatal-error-unsupported-operand-types>`_.


Suggestions
___________

* Make sure all the planned operations are compatible with the type used.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UnsupportedOperandTypes                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>`    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | plus                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


