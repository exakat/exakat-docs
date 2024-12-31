.. _structures-uselistwithforeach:

.. _use-list-with-foreach:

Use List With Foreach
+++++++++++++++++++++

.. meta\:\:
	:description:
		Use List With Foreach: Foreach() structures accepts list() as blind key.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use List With Foreach
	:twitter:description: Use List With Foreach: Foreach() structures accepts list() as blind key
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use List With Foreach
	:og:type: article
	:og:description: Foreach() structures accepts list() as blind key
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/UseListWithForeach.html
	:og:locale: en
  `Foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ structures accepts `list() <https://www.php.net/list>`_ as blind key. If the loop-value is an array with a fixed structure, it is possible to extract the values directly into variables with explicit names.

.. code-block:: php
   
   <?php
   
   // Short way to assign variables
   // Works on PHP 7.1, where list() accepts keys.
   foreach($names as list('first' => $first, 'last' => $last)) {
       doSomething($first, $last);
   }
   
   // Short way to assign variables
   // Works on all PHP versions with numerically indexed arrays.
   foreach($names as list($first, $last)) {
       doSomething($first, $last);
   }
   
   // Long way to assign variables
   foreach($names as $name) {
       $first = $name['first'];
       $last = $name['last'];
       
       doSomething($first, $last);
   }
   
   ?>

See also `list <https://www.php.net/manual/en/function.list.php>`_ and `foreach <https://www.php.net/manual/en/control-structures.foreach.php>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Use the list keyword (or the short syntax), and simplify the array calls in the loop.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UseListWithForeach                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.4                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-mediawiki-structures-uselistwithforeach`                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


