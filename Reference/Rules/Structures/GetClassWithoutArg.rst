.. _structures-getclasswithoutarg:

.. _get\_class()-without-argument:

get_class() Without Argument
++++++++++++++++++++++++++++

.. meta::
	:description:
		get_class() Without Argument: get_class() and get_parent_class() should not be called without arguments.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: get_class() Without Argument
	:twitter:description: get_class() Without Argument: get_class() and get_parent_class() should not be called without arguments
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: get_class() Without Argument
	:og:type: article
	:og:description: get_class() and get_parent_class() should not be called without arguments
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/get_class() Without Argument.html
	:og:locale: en
`get_class() <https://www.php.net/get_class>`_ and `get_parent_class() <https://www.php.net/get_parent_class>`_ should not be called without arguments. It was possible until PHP 8.3, but it is now a deprecated behavior.

.. code-block:: php
   
   <?php
   
   $a = new stdClass;
   
   print get_class($a);
   
   ?>

Suggestions
___________

* Use get_called_class() instead
* Use __CLASS__ magic constant instead




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/GetClassWithoutArg                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP83 <ruleset-CompatibilityPHP83>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.1                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 9.0 and older                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


