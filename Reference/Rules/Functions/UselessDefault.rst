.. _functions-uselessdefault:

.. _useless-default-argument:

Useless Default Argument
++++++++++++++++++++++++

  One of the argument has a default value, and this default value is never used. Every time the method is called, the argument is provided explicitly, rendering the default value actually useless.

.. code-block:: php
   
   <?php
   
   function goo($a, $b = 3) { 
       // do something here
   }
   
   // foo is called 3 times, and sometimes, $b is not provided. 
   goo(1,2);
   goo(1,2);
   goo(1);
   
   
   function foo($a, $b = 3) { 
       // do something here
   }
   
   // foo is called 3 times, and $b is always provided. 
   foo(1,2);
   foo(1,2);
   foo(1,2);
   ?>

Suggestions
___________

* Remove the default value
* Remove the explicit argument in the function call, when it is equal to the default value




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UselessDefault                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | function, default                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


