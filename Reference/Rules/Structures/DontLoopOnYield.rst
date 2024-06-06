.. _structures-dontlooponyield:

.. _don't-loop-on-yield:

Don't Loop On Yield
+++++++++++++++++++

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
| Features     | yield                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolibarr-structures-dontlooponyield`, :ref:`case-tikiwiki-structures-dontlooponyield`                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


