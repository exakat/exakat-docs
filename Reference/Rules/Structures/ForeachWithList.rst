.. _structures-foreachwithlist:

.. _foreach-with-list():

Foreach With list()
+++++++++++++++++++

.. meta::
	:description:
		Foreach With list(): Foreach loops have the ability to use list() (or []) as blind variables.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Foreach With list()
	:twitter:description: Foreach With list(): Foreach loops have the ability to use list() (or []) as blind variables
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Foreach With list()
	:og:type: article
	:og:description: Foreach loops have the ability to use list() (or []) as blind variables
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/ForeachWithList.html
	:og:locale: en
Foreach loops have the ability to use `list() <https://www.php.net/list>`_ (or []) as blind variables. This syntax assign directly array elements to various variables. 

PHP 5.5 introduced the usage of list in `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ loops. Until PHP 7.1, it was not possible to use non-numerical arrays as `list() <https://www.php.net/list>`_ wouldn't support string-indexed arrays.
Previously, it was compulsory to `extract() <https://www.php.net/extract>`_ the data from the blind array :

.. code-block:: php
   
   <?php
       // PHP 5.5 and later, with numerically-indexed arrays
       foreach($array as list($a, $b)) { 
           // do something 
       }
   
   
       // PHP 7.1 and later, with arrays
       foreach($array as list('col1' => $a, 'col3' => $b)) { // 'col2 is ignored'
           // do something 
       }
   ?>

See also `The list function & practical uses of array destructuring in PHP <https://sebastiandedeyne.com/the-list-function-and-practical-uses-of-array-destructuring-in-php>`_ and `Array destructuring in PHP <https://stitcher.io/blog/array-destructuring-with-list-in-php#in-loops>`_.

Connex PHP features
-------------------

  + `foreach <https://php-dictionary.readthedocs.io/en/latest/dictionary/foreach.ini.html>`_


Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ForeachWithList                                                                                                                                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.5 and more recent                                                                                                                                                                 |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


