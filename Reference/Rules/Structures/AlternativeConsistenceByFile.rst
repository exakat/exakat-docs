.. _structures-alternativeconsistencebyfile:

.. _alternative-syntax-consistence:

Alternative Syntax Consistence
++++++++++++++++++++++++++++++

  PHP allows for two syntax : the alternative syntax, and the classic syntax. 

The classic syntax is almost always used. When used, the alternative syntax is used in templates. 

This analysis reports files that are using both syntax at the same time. This is confusing.


.. code-block:: php
   
   <?php
   
   // Mixing both syntax is confusing.
   foreach($array as $item) : 
       if ($item > 1) {
           print "$item elementsn";
       } else {
           print "$item elementn";
       }
   endforeach;
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/AlternativeConsistenceByFile                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.2                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | alternative-syntax                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


