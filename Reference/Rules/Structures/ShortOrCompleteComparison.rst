.. _structures-shortorcompletecomparison:

.. _short-or-complete-comparison:

Short Or Complete Comparison
++++++++++++++++++++++++++++

  Which type of condition is used for boolean comparisons : either short or formal. 

Formal is an explicit comparison to another boolean, while short is when the variable is used without comparison. 

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make them all the same. 


.. code-block:: php
   
   <?php
   
   // returns a boolean
   $checked = checkSomething(); 
   
   // short comparison
   if ($checked) {
   	// doSomething()
   }
   
   // also short comparison
   if (!$checked) {
   	// doSomething()
   }
   
   // formal comparison
   if ($checked === true) {
   	// doSomething()
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ShortOrCompleteComparison                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Preferences <ruleset-Preferences>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


