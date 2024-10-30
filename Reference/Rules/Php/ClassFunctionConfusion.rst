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
Connex PHP features
-------------------

  + `function <https://php-dictionary.readthedocs.io/en/latest/dictionary/function.ini.html>`_
  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


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
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>`      |
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
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


