.. _attributes-phpnativeattributes:

.. _php-native-attributes:

PHP Native Attributes
+++++++++++++++++++++

  This is the list of the PHP native `attribute <https://www.php.net/attribute>`_ in use in the code. PHP native `attribute <https://www.php.net/attribute>`_ depends on the PHP version, as new attributes are added regularly. 

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


