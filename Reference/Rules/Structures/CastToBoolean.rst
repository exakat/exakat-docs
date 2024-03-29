.. _structures-casttoboolean:

.. _cast-to-boolean:

Cast To Boolean
+++++++++++++++

  This expression may be reduced to casting to a boolean. This makes the code more readable, and adapt the type of the value to its usage.

.. code-block:: php
   
   <?php
   
   $variable = $condition == 'met' ? 1 : 0;
   // Same as 
   $variable = (bool) $condition == 'met';
   
   $variable = $condition == 'met' ? 0 : 1;
   // Same as (Note the condition inversion)
   $variable = (bool) $condition != 'met';
   // also, with an indentical condition
   $variable = !(bool) $condition == 'met';
   
   // This also works with straight booleans expressions
   $variable = $condition == 'met' ? true : false;
   // Same as 
   $variable = $condition == 'met';
   
   ?>

Suggestions
___________

* Remove the old expression and use ``(bool)`` operator instead
* Change the target values from true/false, or 0/1 to non-binary values, like strings or integers beyond 0 and 1.
* Complete the current branches with other commands




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CastToBoolean                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | cast                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-mediawiki-structures-casttoboolean`, :ref:`case-dolibarr-structures-casttoboolean`                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


