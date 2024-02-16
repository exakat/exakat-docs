.. _constants-inconsistantcase:

.. _true-false-inconsistant-case:

True False Inconsistant Case
++++++++++++++++++++++++++++

  `TRUE <https://www.php.net/TRUE>`_ or true or True is the favorite.

Usually, PHP projects choose between ALL CAPS True/False, or all lowercase True/False. Sometimes, the project will have no recommendations. 

When your project use a vast majority of one of the convention, then the analyzer will report all remaining inconsistently cased constant. 


.. code-block:: php
   
   <?php
   
   $a1 = true;
   $a2 = true;
   $a3 = true;
   $a4 = true;
   $a5 = true;
   $a6 = true;
   $a7 = true;
   $a8 = true;
   $a9 = true;
   $a10 = true;
   
   // This convention is inconsistence with the rest
   $b1 = TRUE;
   ?>

See also `PHP Constants <https://www.php.net/manual/en/language.constants.php>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/InconsistantCase                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Preferences <ruleset-Preferences>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | constant                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


