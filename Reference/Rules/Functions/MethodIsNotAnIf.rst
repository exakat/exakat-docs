.. _functions-methodisnotanif:

.. _method-is-not-an-if:

Method Is Not An If
+++++++++++++++++++

  When a method consists only in one if statement, it might be worth refactoring. 

Each of the blocks of the if/then structure may be turned into their own method, so has to keep operations distinct. 

Then, the condition can be used as part of a larger method.

.. code-block:: php
   
   <?php
   
   function foo($a) {
   	if ($a === 1) {
   		return 1;
   	} else {
   		return 2;
   	}
   }
   
   ?>

Suggestions
___________

* Export the blocks to distinct functions
* Bail out early




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/MethodIsNotAnIf                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


