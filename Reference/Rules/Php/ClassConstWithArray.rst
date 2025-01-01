.. _php-classconstwitharray:

.. _class-const-with-array:

Class Const With Array
++++++++++++++++++++++

.. meta::
	:description:
		Class Const With Array: This rule lists global and class constant that are defined with an array value.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Class Const With Array
	:twitter:description: Class Const With Array: This rule lists global and class constant that are defined with an array value
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Class Const With Array
	:og:type: article
	:og:description: This rule lists global and class constant that are defined with an array value
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/ClassConstWithArray.html
	:og:locale: en
This rule lists global and class constant that are defined with an array value. This feature was added in PHP 5.6.

.. code-block:: php
   
   <?php
   
   const MY_ARRAY = array();
   
   class x {
   	const MY_OTHER_ARRAY = [1, 2];
   }
   ?>
Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Constants+may+only+evaluate+to+scalar+values.html>`_



Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Suggestions
___________

* Store the array in a variable
* Upgrade to PHP 7.0 or more recent




Specs
_____

+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/ClassConstWithArray                                                                                                                                                                                                                              |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>` |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                                                                                                                                |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 5.5 and more recent                                                                                                                                                                                                                         |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Critical                                                                                                                                                                                                                                             |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Slow (1 hour)                                                                                                                                                                                                                                        |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 5.6                                                                                                                                                                                                                                              |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                                                                                            |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                              |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


