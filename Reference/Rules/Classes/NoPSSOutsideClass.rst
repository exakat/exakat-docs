.. _classes-nopssoutsideclass:

.. _self,-parent,-static-outside-class:

self, parent, static Outside Class
++++++++++++++++++++++++++++++++++

  `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_, `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ and `static <https://www.php.net/manual/en/language.oop5.static.php>`_ should be called inside a class or trait. PHP lint won't report those situations. 

`self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_, `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ and `static <https://www.php.net/manual/en/language.oop5.static.php>`_ may be used in a trait : their actual value will be only known at execution time, when the trait is used.


.. code-block:: php
   
   <?php
   // In the examples, self, parent and static may be used interchangeably
   
   // This raises a Fatal error
   //Fatal error: Uncaught Error: Cannot access static:: when no class scope is active
   new static();
   
   // static calls
   echo self::CONSTANTE;
   echo self::$property;
   echo self::method();
   
   // as a type hint
   function foo(static $x) {
       doSomething();
   }
   
   // as a instanceof
   if ($x instanceof static) {
       doSomething();
   }
   
   ?>


Such syntax problem is only revealed at execution time : PHP raises a Fatal `error <https://www.php.net/error>`_. 

The origin of the problem is usually a method that was moved outside a class, at least temporarily. 

Closures and arrow functions are reported here, though they might be rebound with a valid context before execution.

See also `Scope Resolution Operator (::) <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_.


Suggestions
___________

* Remove the call to static, parent or self
* Make sure the closure is correctly binded before usage




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/NoPSSOutsideClass                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`LintButWontExec <ruleset-LintButWontExec>`            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.3                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | self, parent, static                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


