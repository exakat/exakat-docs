.. _structures-infiniterecursion:

.. _infinite-recursion:

Infinite Recursion
++++++++++++++++++

.. meta::
	:description:
		Infinite Recursion: A method is calling itself, with unchanged arguments.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Infinite Recursion
	:twitter:description: Infinite Recursion: A method is calling itself, with unchanged arguments
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Infinite Recursion
	:og:type: article
	:og:description: A method is calling itself, with unchanged arguments
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/InfiniteRecursion.html
	:og:locale: en
A method is calling itself, with unchanged arguments. This might repeat indefinitely.

This rules applies to recursive functions without any condition. This also applies to function which inject the incoming arguments, without modifications.

.. code-block:: php
   
   <?php
   
   function foo($a, $b) {
       if ($a > 10) {
           return;
       }
       foo($a, $b);
   }
   
   function foo2($a, $b) {
       ++$a;   // $a is modified
       if ($a > 10) {
           return;
       }
       foo2($a, $b);
   }
   
   ?>
Connex PHP features
-------------------

  + `loop <https://php-dictionary.readthedocs.io/en/latest/dictionary/loop.ini.html>`_
  + `recursion <https://php-dictionary.readthedocs.io/en/latest/dictionary/recursion.ini.html>`_
  + `infinite <https://php-dictionary.readthedocs.io/en/latest/dictionary/infinite.ini.html>`_


Suggestions
___________

* Modify arguments before injecting them again in the same method
* Use different values when calling the same method




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/InfiniteRecursion                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


