.. _php-scalartypehintusage:

.. _scalar-typehint-usage:

Scalar Typehint Usage
+++++++++++++++++++++

.. meta\:\:
	:description:
		Scalar Typehint Usage: Spot usage of scalar type hint : ``int``, ``float``, ``boolean`` and ``string``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Scalar Typehint Usage
	:twitter:description: Scalar Typehint Usage: Spot usage of scalar type hint : ``int``, ``float``, ``boolean`` and ``string``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Scalar Typehint Usage
	:og:type: article
	:og:description: Spot usage of scalar type hint : ``int``, ``float``, ``boolean`` and ``string``
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/ScalarTypehintUsage.html
	:og:locale: en
  Spot usage of scalar type hint : ``int``, ``float``, ``boolean`` and ``string``.

Scalar typehint are PHP 7.0 and more recent. Some, like ``object``, is 7.2.

Scalar typehint were not supported in PHP 5 and older. Then, the typehint is treated as a class name.

.. code-block:: php
   
   <?php
   
   function withScalarTypehint(string $x) {}
   
   function withoutScalarTypehint(someClass $x) {}
   
   ?>

See also `PHP RFC: Scalar Type Hints <https://wiki.php.net/rfc/scalar_type_hints>`_ and `Type declarations <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration>`_.

Connex PHP features
-------------------

  + `scalar-typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/scalar-typehint.ini.html>`_
  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_


Specs
_____

+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/ScalarTypehintUsage                                                                                                                                                                 |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 7.0 and more recent                                                                                                                                                            |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Major                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                                                                         |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.0                                                                                                                                                                                 |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                               |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


