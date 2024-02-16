.. _classes-missingabstractmethod:

.. _missing-abstract-method:

Missing Abstract Method
+++++++++++++++++++++++

  Abstract methods must have a non-abstract version for the class to be complete. A class that is missing one abstract definition cannot be instantiated.

.. code-block:: php
   
   <?php
   
   // This is a valid definition
   class b extends a {
       function foo() {}
       function bar() {}
   }
   
   // This compiles, but will emit a fatal error if instantiated
   class c extends a {
       function bar() {}
   }
   
   // This illustration lint but doesn't run.
   // moving this class at the beginning of the code will make lint fail
   abstract class a {
       abstract function foo() ;
   }
   
   ?>

See also `Classes Abstraction <https://www.php.net/abstract>`_.


Suggestions
___________

* Implement the missing methods
* Remove the partially implemented class
* Mark the partially implemented class abstract




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MissingAbstractMethod                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | abstract                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


