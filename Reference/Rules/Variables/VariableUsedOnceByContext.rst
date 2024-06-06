.. _variables-variableusedoncebycontext:

.. _used-once-variables-(in-scope):

Used Once Variables (In Scope)
++++++++++++++++++++++++++++++

  This is the list of used once variables, scope by scope. Those variables are used once in a function, a method, a class or a namespace. In any case, this means the variable is read or written, while it should be used at least twice. 

`Static <https://www.php.net/manual/en/language.oop5.static.php>`_ and global variables are omitted here : they may be used multiple times by having the method being called multiple times. 

Blind variables, which are defined in a `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ structure, are also omitted : the loop will use them multiple time, assigning different values each time.

Parameters that are inherited from `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ classes' methods are also omitted : they are imposed by the structure, and cannot be avoided.

.. code-block:: php
   
   <?php
   
   function foo() {
       // The variables below never appear twice, inside foo()
       $writtenOnce = 1;
   
       foo($readOnce);
       // They do appear again in other functions, or in global space. 
   }
   
   function bar() {
       $writtenOnce = 1;
       foo($readOnce);
   }
   
   ?>

Suggestions
___________

* Remove the variable
* Fix the name of variable
* Use the variable a second time in the current scope, at least




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/VariableUsedOnceByContext                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | static-variable                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-shopware-variables-variableusedoncebycontext`                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


