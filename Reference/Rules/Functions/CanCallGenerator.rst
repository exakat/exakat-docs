.. _functions-cancallgenerator:

.. _can't-call-generator:

Can't Call Generator
++++++++++++++++++++

  It is not possible to call directly a `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_, aka a method that uses the yield keyword. Such structure shall be used directly in a `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ structure, or with the function ``iterator_to_array()``.

.. code-block:: php
   
   <?php
   
   function foo() {
   	echo __FUNCTION__;
   	yield 1;
   }
   
   // Won't display anything, even 'foo'
   foo(); 
   
   // displays both foo and 1
   foreach(foo() as $g) {
   	print $g;
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/CanCallGenerator                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.3                                                                                                                   |
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


