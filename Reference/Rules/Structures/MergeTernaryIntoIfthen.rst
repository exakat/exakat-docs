.. _structures-mergeternaryintoifthen:

.. _could-merge-ternary-into-ifthen:

Could Merge Ternary Into Ifthen
+++++++++++++++++++++++++++++++

  When two ternary operators are used, in succession, with the same condition, it might be more readable to write it as an if then condition.

With an if then structure, the related instructions are grouped together, while they are scattered otherwise.

Readability improves with more ternaries in a row.

.. code-block:: php
   
   <?php
   
   $variable1 = $a ? 'b0' : $c;
   $variable2 = $a ? foo() : null;
   
   if ($a) {
   	$variable1 = 'b0';
   	$variable2 = foo();
   } else {
   	$variable1 = $c;
   	$variable2 = null;
   }
   
   ?>
Connex PHP features
-------------------

  + `ternary <https://php-dictionary.readthedocs.io/en/latest/dictionary/ternary.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MergeTernaryIntoIfthen                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.8                                                                                                                   |
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


