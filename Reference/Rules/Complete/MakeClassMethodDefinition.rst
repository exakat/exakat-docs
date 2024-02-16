.. _complete-makeclassmethoddefinition:

.. _make-class-method-definition:

Make Class Method Definition
++++++++++++++++++++++++++++

  This command links a method call to its method definition. 


.. code-block:: php
   
   <?php
   
   class x {
       function foo() {
           // This links to the bar() method
           return $this->bar();
       }
   
       function bar() {
           // This links to the link() method
           return $this->bar();
       }
   }
   
   ?>


This command may not detect all possible link for the methods. It may be missing information about the nature of the object.

This command may also produce multiple definitions link, when the definition are ambiguous.

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/MakeClassMethodDefinition                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`NoDoc <ruleset-NoDoc>`                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                   |
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


