.. _structures-dontlooponyield:

.. _don't-loop-on-yield:

Don't Loop On Yield
+++++++++++++++++++

.. meta::
	:description:
		Don't Loop On Yield: Use ``yield from``, instead of looping on a generator with ``yield``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Don't Loop On Yield
	:twitter:description: Don't Loop On Yield: Use ``yield from``, instead of looping on a generator with ``yield``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Don't Loop On Yield
	:og:type: article
	:og:description: Use ``yield from``, instead of looping on a generator with ``yield``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Don't Loop On Yield.html
	:og:locale: en
Use ``yield from``, instead of looping on a `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_ with ``yield``.

``yield from`` delegate the yielding to another `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_, and keep calling that `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_ until it is finished. It also works with implicit `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_ datastructure, like arrays.
There is a performance gain when delegating, over looping manually on the `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_. You may even consider writing the loop to store all values in an array, then ``yield from`` the array.

.. code-block:: php
   
   <?php
   
   function generator() {
       for($i = 0; $i < 10; ++$i) {
           yield $i;
       }
   }
   
   function delegatingGenerator() {
       yield from generator();
   }
   
   // Too much code here
   function generator2() {
       foreach(generator() as $g) {
           yield $g;
       }
   }
   
   ?>

See also `Generator delegation via yield from <https://www.php.net/manual/en/language.generators.syntax.php#control-structures.yield.from>`_.

Connex PHP features
-------------------

  + `yield <https://php-dictionary.readthedocs.io/en/latest/dictionary/yield.ini.html>`_


Suggestions
___________

* Use `yield from` instead of the whole foreach() loop




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DontLoopOnYield                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolibarr-structures-dontlooponyield`, :ref:`case-tikiwiki-structures-dontlooponyield`                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


