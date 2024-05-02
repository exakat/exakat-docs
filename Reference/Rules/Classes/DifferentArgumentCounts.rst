.. _classes-differentargumentcounts:

.. _different-argument-counts:

Different Argument Counts
+++++++++++++++++++++++++

  Two methods with the same name shall have the same number of compulsory argument. PHP accepts different number of arguments between two methods, if the extra arguments have default values. Basically, they shall be called interchangeably with the same number of arguments.

The number of compulsory arguments is often mistaken for the same number of arguments. When this is the case, it leads to confusion between the two signatures. It will also create more difficulties when refactoring the signature.

While this code is legit, it is recommended to check if the two signatures could be synchronized, and reduce future surprises.

.. code-block:: php
   
   <?php
   
   class x {
       function foo($a ) {}
   }
   
   class y extends x {
       // This method is compatible with the above, its signature is different
       function foo($a, $b = 1) {}
   }
   
   ?>

Suggestions
___________

* Extract the extra arguments into other methods
* Remove the extra arguments
* Add the extra arguments to all the signatures




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/DifferentArgumentCounts                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | method                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


