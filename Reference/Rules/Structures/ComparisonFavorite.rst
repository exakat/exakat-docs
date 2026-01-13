.. _structures-comparisonfavorite:

.. _strict-or-relaxed-comparison:

Strict Or Relaxed Comparison
++++++++++++++++++++++++++++

  PHP has two comparison styles : strict and relaxed. 

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make them all the same. 

It is recommended to always use the strict comparison by default, and use the relaxed in case of specific situations.

.. code-block:: php
   
   <?php
   
   // This compares $strict both in terms of value and type
   if ($strict === 3) {
   
   } elseif ($strict == 3) {
       // This compares $strict after an possible type casting. 
       // '3', 3.0 or 3 would all be possible solutions.
   }
   
   ?>

See also `Comparison Operators <https://www.php.net/manual/en/language.operators.comparison.php>`_.

Connex PHP features
-------------------

  + `comparison <https://php-dictionary.readthedocs.io/en/latest/dictionary/comparison.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ComparisonFavorite                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


