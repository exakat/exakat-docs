.. _functions-nullablewithconstant:

.. _nullable-with-constant:

Nullable With Constant
++++++++++++++++++++++

.. meta::
	:description:
		Nullable With Constant: Arguments are automatically nullable with a literal null.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Nullable With Constant
	:twitter:description: Nullable With Constant: Arguments are automatically nullable with a literal null
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Nullable With Constant
	:og:type: article
	:og:description: Arguments are automatically nullable with a literal null
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Nullable With Constant.html
	:og:locale: en
Arguments are automatically nullable with a literal null. They used to also be nullable with a constant null, before PHP 8.0.

.. code-block:: php
   
   <?php
   
   // Extracted from https://github.com/php/php-src/blob/master/UPGRADING
   
   // Replace
   function test(int $arg = CONST_RESOLVING_TO_NULL) {}
   // With
   function test(?int $arg = CONST_RESOLVING_TO_NULL) {}
   // Or
   function test(int $arg = null) {}
           
   ?>
Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Suggestions
___________

* Use the valid syntax




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/NullableWithConstant                                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>`                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.9                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.2 and older                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


