.. _functions-functioncalledwithothercase:

.. _function-called-with-other-case-than-defined:

Function Called With Other Case Than Defined
++++++++++++++++++++++++++++++++++++++++++++

  Functions and methods are defined with a specific case. Often, this is done on purpose,
either to distinguish the method from others, such as PHP natives functions, or to follow a naming
convention. 

PHP functions are case insensitive, which leads to situations like : 
It is recommended to use the same casing in the function call and the function definition.

.. code-block:: php
   
   <?php
     function myUtility($arg) { 
       /* some code here */
     } 
   
      myutility($var);
   ?>

Suggestions
___________

* Use the same case for the function and its call.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/FunctionCalledWithOtherCase                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Semantics <ruleset-Semantics>`                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | function                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


