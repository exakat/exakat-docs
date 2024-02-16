.. _structures-commonalternatives:

.. _common-alternatives:

Common Alternatives
+++++++++++++++++++

  In the following conditional structures, expressions were found that are common to both 'then' and 'else'. It may be interesting, though not always possible, to put them both out of the conditional, and reduce line count. 


.. code-block:: php
   
   <?php
   if ($c == 5) {
       $b = strtolower($b[2]); 
       $a++;
   } else {
       $b = strtolower($b[2]); 
       $b++;
   }
   ?>


may be rewritten in : 


.. code-block:: php
   
   <?php
   
   $b = strtolower($b[2]); 
   if ($c == 5) {
       $a++;
   } else {
       $b++;
   }
   
   ?>

Suggestions
___________

* Collect common expressions, and move them before of after the if/then expression.
* Move a prefix and suffixes to a third-party method




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CommonAlternatives                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolibarr-structures-commonalternatives`, :ref:`case-nextcloud-structures-commonalternatives`                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


