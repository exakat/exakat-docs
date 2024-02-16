.. _structures-misusedyield:

.. _misused-yield:

Misused Yield
+++++++++++++

  When chaining `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_, one must use the yield from keyword.

Forgetting the yield from keyword cancels the `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_ nature of the functioncall and nothing is emited. 

Using ``yield`` on a `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_, yields `... <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_ the `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_, not the values of the `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_.


.. code-block:: php
   
   <?php
   
   function foo() {
   	yield 1;
   	// Goo is called, but not run as a generator
   	goo();
   }
   
   function hoo() {
   	yield 1;
   	// Goo is yield, but not run as a generator
   	yield goo();
   }
   
   function goo() {
   	yield 3;
   }
   
   ?>


It is legit to yield a `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_, for later usage. This is just very uncommon, and worth a check.

Suggestions
___________

* Use the yield from keyword




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MisusedYield                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | yield-from                                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


