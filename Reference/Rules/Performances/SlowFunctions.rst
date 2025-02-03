.. _performances-slowfunctions:

.. _slow-functions:

Slow Functions
++++++++++++++

.. meta::
	:description:
		Slow Functions: Avoid using those slow native PHP functions, and replace them with alternatives.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Slow Functions
	:twitter:description: Slow Functions: Avoid using those slow native PHP functions, and replace them with alternatives
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Slow Functions
	:og:type: article
	:og:description: Avoid using those slow native PHP functions, and replace them with alternatives
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Slow Functions.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/SlowFunctions.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/SlowFunctions.html","name":"Slow Functions","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Avoid using those slow native PHP functions, and replace them with alternatives","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Slow Functions.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Avoid using those slow native PHP functions, and replace them with alternatives.
+---------------------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------+
| Slow Function                                                 |  Faster                                                                                                                    | 
+---------------------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------+
| `array_diff() <https://www.php.net/array_diff>`_              |  `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_                                               | 
| `array_intersect() <https://www.php.net/array_intersect>`_    |  `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_                                               | 
| `array_key_exists() <https://www.php.net/array_key_exists>`_  |  `isset() <https://www.www.php.net/isset>`_ and `array_key_exists() <https://www.php.net/array_key_exists>`_               | 
| `array_map() <https://www.php.net/array_map>`_                |  `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_                                               | 
| `array_search() <https://www.php.net/array_search>`_          |  `array_flip() <https://www.php.net/array_flip>`_ and `isset() <https://www.www.php.net/isset>`_                           | 
| `array_udiff() <https://www.php.net/array_udiff>`_            |  Use another way                                                                                                           | 
| `array_uintersect() <https://www.php.net/array_uintersect>`_  |  Use another way                                                                                                           | 
| `array_unshift() <https://www.php.net/array_unshift>`_        |  Use another way                                                                                                           | 
| `array_walk() <https://www.php.net/array_walk>`_              |  `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_                                               | 
| `in_array() <https://www.php.net/in_array>`_                  |  `isset() <https://www.www.php.net/isset>`_                                                                                | 
| `preg_replace() <https://www.php.net/preg_replace>`_          |  `strpos() <https://www.php.net/strpos>`_                                                                                  | 
| `strstr() <https://www.php.net/strstr>`_                      |  `strpos() <https://www.php.net/strpos>`_                                                                                  | 
| `uasort() <https://www.php.net/uasort>`_                      |  Use another way                                                                                                           | 
| `uksort() <https://www.php.net/uksort>`_                      |  Use another way                                                                                                           | 
| `usort() <https://www.php.net/usort>`_                        |  Use another way                                                                                                           | 
| `array_unique() <https://www.php.net/array_unique>`_          |  `array_keys() <https://www.php.net/array_keys>`_ and `array_count_values() <https://www.php.net/array_count_values>`_     | 
+---------------------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------+

`array_unique() <https://www.php.net/array_unique>`_ has been accelerated in PHP 7.2 and may be used directly from this version on : `Optimize `array_unique() <https://www.php.net/array_unique>`_ <https://github.com/php/php-src/commit/6c2c7a023da4223e41fea0225c51a417fc8eb10d>`_.

`array_key_exists() <https://www.php.net/array_key_exists>`_ has been accelerated in PHP 7.4 and may be used directly from this version on : `Implement ZEND_ARRAY_KEY_EXISTS opcode to speed up `array_key_exists() <https://www.php.net/array_key_exists>`_ <https://github.com/php/php-src/pull/3360>`_.

.. code-block:: php
   
   <?php
   
   $array = source();
   
   // Slow extraction of distinct values
   $array = array_unique($array);
   
   // Much faster extraction of distinct values
   $array = array_keys(array_count_values($array));
   
   ?>

Suggestions
___________

* Replace the slow function with a faster version
* Remove the usage of the slow function




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/SlowFunctions                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `avoid-those-slow-functions <https://github.com/dseguy/clearPHP/tree/master/rules/avoid-those-slow-functions.md>`__      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-churchcrm-performances-slowfunctions`, :ref:`case-suitecrm-performances-slowfunctions`                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


