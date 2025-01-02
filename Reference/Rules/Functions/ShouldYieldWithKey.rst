.. _functions-shouldyieldwithkey:

.. _should-yield-with-key:

Should Yield With Key
+++++++++++++++++++++

.. meta::
	:description:
		Should Yield With Key: iterator_to_array() overwrite generated values with the same key.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Should Yield With Key
	:twitter:description: Should Yield With Key: iterator_to_array() overwrite generated values with the same key
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Should Yield With Key
	:og:type: article
	:og:description: iterator_to_array() overwrite generated values with the same key
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Should Yield With Key.html
	:og:locale: en
`iterator_to_array() <https://www.php.net/iterator_to_array>`_ overwrite generated values with the same key. 

PHP generators are based on the ``yield`` keyword. They also delegate some generating to other methods, with ``yield from``. 

When delegating, ``yield from`` uses the keys that are generated with ``yield``, and otherwise, it uses auto-generated index, starting with 0. 

The trap is that each ``yield from`` reset the index generation and start again with 0. Coupled with `iterator_to_array() <https://www.php.net/iterator_to_array>`_, this means that the final generated array may lack some values, while a `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ loop would yield all of them.

Thanks to `Holger Woltersdorf <https://twitter.com/hollodotme>`_ for `pointing this <https://twitter.com/hollodotme/status/1057909890566537217>`_.

.. code-block:: php
   
   <?php 
   
   function g1() : Generator {
   	for ( $i = 0; $i < 4; $i++ ) { yield $i; }
   }
   
   function g2() : Generator {
   	for ( $i = 5; $i < 10; $i++ ) { yield $i; }
   }
   
   function aggregator() : Generator {
   	yield from g1();
   	yield from g2();
   }
   
   print_r(iterator_to_array());
   
   /*
   Array
   (
       [0] => 6
       [1] => 7
       [2] => 8
       [3] => 9
       [4] => 4  // Note that 4 and 5 still appears
       [5] => 5  // They are not overwritten by the second yield
   )
   */
   
   
   foreach ( aggregator() as $i ) {
   	print $i.PHP_EOL;
   }
   
   /*
   0  // Foreach has no overlap and yield it all.
   1
   2
   3
   4
   5
   6
   7
   8
   9
   */
   
   ?>

See also `Generator syntax <https://www.php.net/manual/en/language.generators.syntax.php>`_ and `Yielding values with keys <https://www.php.net/manual/en/language.generators.syntax.php#control-structures.yield.associative>`_.

Connex PHP features
-------------------

  + `yield <https://php-dictionary.readthedocs.io/en/latest/dictionary/yield.ini.html>`_
  + `key <https://php-dictionary.readthedocs.io/en/latest/dictionary/key.ini.html>`_


Suggestions
___________

* Use iterator_to_array() on each generator separately, and use array_merge() to merge all the arrays.
* Always yield with distinct keys
* Avoid iterator_to_array() and use foreach()




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/ShouldYieldWithKey                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Top10 <ruleset-Top10>`                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.2                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


