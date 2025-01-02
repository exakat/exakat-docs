.. _structures-dereferencingas:

.. _dereferencing-string-and-arrays:

Dereferencing String And Arrays
+++++++++++++++++++++++++++++++

.. meta::
	:description:
		Dereferencing String And Arrays: PHP allows the direct dereferencing of strings and arrays, from array literals and returned array.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Dereferencing String And Arrays
	:twitter:description: Dereferencing String And Arrays: PHP allows the direct dereferencing of strings and arrays, from array literals and returned array
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Dereferencing String And Arrays
	:og:type: article
	:og:description: PHP allows the direct dereferencing of strings and arrays, from array literals and returned array
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Dereferencing String And Arrays.html
	:og:locale: en
PHP allows the direct dereferencing of strings and arrays, from array literals and returned array. 

This was added in PHP 5.5. There is no need anymore for an intermediate variable between a string and array (or any expression generating such value) and accessing an index.

.. code-block:: php
   
   <?php
   $x = array(4,5,6); 
   $y = $x[2] ; // is 6
   
   //May be replaced by 
   $y = array(4,5,6)[2];
   $y = [4,5,6][2];
   ?>
Connex PHP features
-------------------

  + `dereferencing <https://php-dictionary.readthedocs.io/en/latest/dictionary/dereferencing.ini.html>`_


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DereferencingAS                                                                                                                                                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.3 and older                                                                                                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


