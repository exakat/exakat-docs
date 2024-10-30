.. _functions-uselessreturn:

.. _useless-return:

Useless Return
++++++++++++++

  The spotted functions or methods have a return statement, but this statement is useless. This is the case for constructor and destructors, whose return value are ignored or inaccessible.

When return is void, and the last element in a function, it is also useless.

.. code-block:: php
   
   <?php
   
   class foo {
       function __construct() {
           // return is not used by PHP
           return 2;
       }
   }
   
   function bar(&$a) {
       $a++;
       // The last return, when empty, is useless
       return;
   }
   
   ?>
Connex PHP features
-------------------

  + `return <https://php-dictionary.readthedocs.io/en/latest/dictionary/return.ini.html>`_


Suggestions
___________

* Remove the return expression. Keep any other calculation.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UselessReturn                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-thinkphp-functions-uselessreturn`, :ref:`case-vanilla-functions-uselessreturn`                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


