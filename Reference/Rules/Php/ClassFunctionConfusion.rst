.. _php-classfunctionconfusion:

.. _class-function-confusion:

Class Function Confusion
++++++++++++++++++++++++

  Avoid classes and functions bearing the same name. 

When functions and classes bear the same name, calling them may be confusing. This may also lead to forgotten 'new' keyword.


.. code-block:: php
   
   <?php
   
   class foo {}
   
   function foo() {}
   
   // Forgetting the 'new' operator is easy
   $object = new foo();
   $object = foo();
   
   ?>

Suggestions
___________

* Use a naming convention to distinguish functions and classes
* Rename the class or the function (or both)
* Use an alias with a `use` expression




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ClassFunctionConfusion                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Semantics <ruleset-Semantics>`                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.2                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | function, class                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


