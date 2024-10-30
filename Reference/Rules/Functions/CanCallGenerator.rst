.. _functions-cancallgenerator:

.. _can't-call-generator:

Can't Call Generator
++++++++++++++++++++

  It is not possible to call directly a generator: a `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_ is a method that uses the ``yield`` or ``yield from`` keyword. 

Such structure shall be used directly in a `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ structure, or with the function ``iterator_to_array()``.

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
Connex PHP features
-------------------

  + `yield <https://php-dictionary.readthedocs.io/en/latest/dictionary/yield.ini.html>`_
  + `yield-from <https://php-dictionary.readthedocs.io/en/latest/dictionary/yield-from.ini.html>`_
  + `generator <https://php-dictionary.readthedocs.io/en/latest/dictionary/generator.ini.html>`_


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


