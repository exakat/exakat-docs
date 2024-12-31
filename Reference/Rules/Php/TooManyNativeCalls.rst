.. _php-toomanynativecalls:

.. _too-many-native-calls:

Too Many Native Calls
+++++++++++++++++++++

.. meta\:\:
	:description:
		Too Many Native Calls: Avoid stuffing too many PHP native call inside another functioncall.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Too Many Native Calls
	:twitter:description: Too Many Native Calls: Avoid stuffing too many PHP native call inside another functioncall
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Too Many Native Calls
	:og:type: article
	:og:description: Avoid stuffing too many PHP native call inside another functioncall
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/TooManyNativeCalls.html
	:og:locale: en
  Avoid stuffing too many PHP native call inside another functioncall. 

For readability reasons, or, more often, for edge case handling, it is recommended to avoid nesting too many PHP native calls. 

This analysis reports any situation where more than 3 PHP native calls are nested.

.. code-block:: php
   
   <?php
   
   // Too many nested functions 
   $cleanArray = array_unique(array_keys(array_count_values(array_column($source, 'x'))));
   
   // Avoid warning when source is empty
   $extract = array_column($source, 'x');
   if (empty($extract)) {
       $cleanArray = array();
   } else {
       $cleanArray = array_unique(array_keys(array_count_values($extract)));
   }
   
   // This is not readable, although it is short. 
   // It may easily get out of hand.
   echo chr(80), chr(72), chr(80), chr(32), ' is great!';
   
   ?>

+------------------+---------+---------+---------------------------------------------------+
| Name             | Default | Type    | Description                                       |
+------------------+---------+---------+---------------------------------------------------+
| nativeCallCounts | 3       | integer | Number of native calls found inside another call. |
+------------------+---------+---------+---------------------------------------------------+


Connex PHP features
-------------------

  + `native <https://php-dictionary.readthedocs.io/en/latest/dictionary/native.ini.html>`_


Suggestions
___________

* Reduce the number of native calls
* Split the method into smaller methods




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/TooManyNativeCalls                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.10                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-spip-php-toomanynativecalls`                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


