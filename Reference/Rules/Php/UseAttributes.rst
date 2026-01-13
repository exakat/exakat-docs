.. _php-useattributes:

.. _use-php-attributes:

Use PHP Attributes
++++++++++++++++++

  This rule reports if PHP 8.0 attributes are in use. 

Attributes look like special comments ``#[`... <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_]``. They are linked to classes, traits, interfaces, enums, class constants, functions, methods, and parameters.


.. code-block:: php
   
   <?php
   
   #[foo(4)]
   class x {
   
   }
   
   ?>

See also `PHP RFC: Shorter Attribute Syntax <https://wiki.php.net/rfc/shorter_attribute_syntax>`_, `Attributes Amendements <https://wiki.php.net/rfc/attribute_amendments>`_ and `Shorter Attribute Syntax Change <https://wiki.php.net/rfc/shorter_attribute_syntax_change>`_.

Connex PHP features
-------------------

  + `attribute <https://php-dictionary.readthedocs.io/en/latest/dictionary/attribute.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseAttributes                                                                                                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.6                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


