.. _structures-nonintstringasindex:

.. _non-integer-nor-string-as-index:

Non Integer Nor String As Index
+++++++++++++++++++++++++++++++

  Report usage of non-integer and non-string types as index in an array syntax.

PHP arrays only accept integers and strings as keys. PHP convert the other types to integer or string, and that may lead to surprises when reading the arrays.

.. code-block:: php
   
   <?php
   
   function foo (float $index, array $array) {
   	$array[$index];
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NonIntStringAsIndex                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Low                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


