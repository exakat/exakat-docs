.. _functions-emptyfunction:

.. _empty-function:

Empty Function
++++++++++++++

  Function or method whose body is empty. 

Such functions or methods are rarely useful. As a bare minimum, the function should return some useful value, even if constant.

A method is considered empty when it contains nothing, or contains expressions without impact. 


.. code-block:: php
   
   <?php
   
   // classic empty function
   function emptyFunction() {}
   
   class bar {
       // classic empty method
       function emptyMethod() {}
   
       // classic empty function
       function emptyMethodWithParent() {}
   }
   
   class barbar extends bar {
       // NOT an empty method : it overwrites the parent method
       function emptyMethodWithParent() {}
   }
   
   ?>


Methods which overwrite another methods are omitted. Methods which are the concrete version of an abstract method are considered.

Suggestions
___________

* Fill the function with actual code
* Remove any usage of the function, then remove the function




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/EmptyFunction                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | function                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-contao-functions-emptyfunction`                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


