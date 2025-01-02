.. _php-returntypehintusage:

.. _return-typehint-usage:

Return Typehint Usage
+++++++++++++++++++++

.. meta::
	:description:
		Return Typehint Usage: Spot usage of return typehint.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Return Typehint Usage
	:twitter:description: Return Typehint Usage: Spot usage of return typehint
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Return Typehint Usage
	:og:type: article
	:og:description: Spot usage of return typehint
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Return Typehint Usage.html
	:og:locale: en
Spot usage of return typehint. It is a PHP 7.0 feature.

Return typehint were introduced in PHP 7.0, and are backward incompatible with PHP 5.x.

.. code-block:: php
   
   <?php
   
   function foo($a) : stdClass {
       return new \stdClass();
   }
   
   ?>

See also `RFC: Return Type Declarations <https://wiki.php.net/rfc/return_types>`_ and `Return Type Declarations <https://www.php.net/manual/en/functions.returning-values.php#functions.returning-values.type-declaration>`_.

Connex PHP features
-------------------

  + `returntype <https://php-dictionary.readthedocs.io/en/latest/dictionary/returntype.ini.html>`_


Specs
_____

+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/ReturnTypehintUsage                                                                                                                                                                 |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 7.0 and more recent                                                                                                                                                            |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         |                                                                                                                                                                                         |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      |                                                                                                                                                                                         |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.0                                                                                                                                                                                 |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                               |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


