.. _structures-sgvariablesconfusion:

.. _static-global-variables-confusion:

Static Global Variables Confusion
+++++++++++++++++++++++++++++++++

  PHP can't have variable that are both `static <https://www.php.net/manual/en/language.oop5.static.php>`_ and global variable. While the syntax is legit, the variables will be alternatively global or `static <https://www.php.net/manual/en/language.oop5.static.php>`_.

It is recommended to avoid using the same name for a global variable and a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ variable.

.. code-block:: php
   
   <?php
   
   function foo() {
       $a = 1; // $a is a local variable
       
       global $a; // $a is now a global variable
       
       static $a; // $a is not w static variable 
   }
   
   ?>

Suggestions
___________

* Avoid using static variables
* Avoid using global variables
* Avoid using the same name for static and global variables




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/SGVariablesConfusion                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Semantics <ruleset-Semantics>`, :ref:`Suggestions <ruleset-Suggestions>`                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | global, static                                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


