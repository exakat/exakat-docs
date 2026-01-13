.. _functions-noreturnused:

.. _no-return-used:

No Return Used
++++++++++++++

  The return value of the following methods are never used. The return argument may be dropped from the code, as it is dead code.

This analysis supports functions and `static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods, when a definition may be found. It doesn't support method calls.

.. code-block:: php
   
   <?php
   
   function foo($a = 1) { return 1; }
   
   foo();
   foo();
   foo();
   foo();
   foo();
   foo();
   
   // This function doesn't return anything. 
   function foo2() { }
   
   // The following function are used in an expression, thus the return is important
   function foo3() {  return 1;}
   function foo4() {  return 1;}
   function foo5() {  return 1;}
   
   foo3() + 1; 
   $a = foo4();
   foo(foo5());
   
   ?>
Connex PHP features
-------------------

  + `return <https://php-dictionary.readthedocs.io/en/latest/dictionary/return.ini.html>`_


Suggestions
___________

* Remove the return statement in the function
* Actually use the value returned by the method, for test or combination with other values




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/NoReturnUsed                                                                                                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.3                                                                                                                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-spip-functions-noreturnused`, :ref:`case-livezilla-functions-noreturnused`                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+


