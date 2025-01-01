.. _php-php72objectkeyword:

.. _php-7.2-object-keyword:

PHP 7.2 Object Keyword
++++++++++++++++++++++

.. meta::
	:description:
		PHP 7.2 Object Keyword: 'object' is a PHP keyword.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP 7.2 Object Keyword
	:twitter:description: PHP 7.2 Object Keyword: 'object' is a PHP keyword
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP 7.2 Object Keyword
	:og:type: article
	:og:description: 'object' is a PHP keyword
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/Php72ObjectKeyword.html
	:og:locale: en
'object' is a PHP keyword. It can't be used for class, interface or trait name. 

This is the case since PHP 7.2.

.. code-block:: php
   
   <?php
   
   // Valid until PHP 7.2
   class object {}
   
   // Altough it is really weird anyway...
   
   ?>

See also `List of Keywords <https://www.php.net/manual/en/reserved.keywords.php>`_.


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php72ObjectKeyword                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP72 <ruleset-CompatibilityPHP72>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.2 and older                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


