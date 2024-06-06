.. _structures-variablemaybenonglobal:

.. _declare-global-early:

Declare Global Early
++++++++++++++++++++

  `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ and global keywords should be used as early as possible in a method. 

Performance wise, it is better to call ``global`` or ``static`` only before using the variable. 

Human-wise, it is recommended to put ``global`` or ``static`` at the beginning of the method, for better readability.

.. code-block:: php
   
   <?php 
   
   function foo() {
       // $a is not global yet. It is a local variable
       $a = 1;
       // Same for static variables
       $s = 5;
   
       // Now $a is global
       global $a;
       $a = 3;
   
       // Now $s is static
       static $s;
       $s = 55;
   }
   
   ?>

See also `Using static variables <https://www.php.net/manual/en/language.variables.scope.php#language.variables.scope.static>`_ and `The global keyword <https://www.php.net/manual/en/language.variables.scope.php#language.variables.scope.global>`_.


Suggestions
___________

* Use static and global at the beginning of the method
* Move static and global to the first usage of the variable
* Remove any access to the variable before static and global




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/VariableMayBeNonGlobal                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | static-variable, global-variable                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


