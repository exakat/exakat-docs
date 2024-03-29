.. _php-wrongattributeconfiguration:

.. _wrong-attribute-configuration:

Wrong Attribute Configuration
+++++++++++++++++++++++++++++

  A class is attributed to the wrong PHP structure.

.. code-block:: php
   
   <?php
   #[Attribute(Attribute::TARGET_CLASS)]
   class ClassAttribute { }
   
   // Wrong
   #[ClassAttribute]
   function foo () {}
   
   // OK
   #[ClassAttribute]
   class y  {}
   
   ?>

See also `Declaring Attribute Classes <https://www.php.net/manual/en/language.attributes.classes.php>`_.


Suggestions
___________

* Remove the attribute from the wrongly attributed structure
* Extend the configuration of the attribute with Attribute::TARGET_*




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/WrongAttributeConfiguration                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | attribute                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


