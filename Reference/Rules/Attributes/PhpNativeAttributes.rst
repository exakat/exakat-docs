.. _attributes-phpnativeattributes:

.. _php-native-attributes:

PHP Native Attributes
+++++++++++++++++++++

.. meta::
	:description:
		PHP Native Attributes: This is the list of the PHP native attribute used in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP Native Attributes
	:twitter:description: PHP Native Attributes: This is the list of the PHP native attribute used in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP Native Attributes
	:og:type: article
	:og:description: This is the list of the PHP native attribute used in the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PHP Native Attributes.html
	:og:locale: en
This is the list of the PHP native `attribute <https://www.php.net/attribute>`_ used in the code. PHP native `attribute <https://www.php.net/attribute>`_ depends on the PHP version, as new attributes are added regularly. 

.. code-block:: php
   
   <?php
   
   #[Attribute]
   class x {
   	function foo(#[SensitiveParameter] $a) {
   		// doSomething()
   	}
   }
   
   ?>

See also `PHP native attributes <https://www.exakat.io/en/php-native-attributes-quick-reference/>`_.

Connex PHP features
-------------------

  + `attribute <https://php-dictionary.readthedocs.io/en/latest/dictionary/attribute.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Attributes/PhpNativeAttributes                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Attributes <ruleset-Attributes>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


