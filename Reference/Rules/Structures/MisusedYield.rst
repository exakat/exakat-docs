.. _structures-misusedyield:

.. _misused-yield:

Misused Yield
+++++++++++++

.. meta::
	:description:
		Misused Yield: When chaining generator, one must use the ``yield from`` keyword.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Misused Yield
	:twitter:description: Misused Yield: When chaining generator, one must use the ``yield from`` keyword
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Misused Yield
	:og:type: article
	:og:description: When chaining generator, one must use the ``yield from`` keyword
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Misused Yield.html
	:og:locale: en
When chaining `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_, one must use the ``yield from`` keyword.

Forgetting the yield from keyword cancels the `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_ nature of the functioncall and nothing is emited. 

Using ``yield`` on a `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_, yields `... <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_ the `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_, not the values of the `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_.

It is legit to yield a `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_, for later usage. This is just very uncommon, and worth a check.

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
Connex PHP features
-------------------

  + `yield-from <https://php-dictionary.readthedocs.io/en/latest/dictionary/yield-from.ini.html>`_


Suggestions
___________

* Use the yield from keyword




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MisusedYield                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
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
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


