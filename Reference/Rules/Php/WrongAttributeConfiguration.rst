.. _php-wrongattributeconfiguration:

.. _wrong-attribute-configuration:

Wrong Attribute Configuration
+++++++++++++++++++++++++++++

  A class is attributed to the wrong PHP structure. A class may be an `attribute <https://www.php.net/attribute>`_, and it may also be configured to be used with different structures : classes, function, parameters, etc. When an `attribute <https://www.php.net/attribute>`_ has a configuration, it must be used with the correct structure.

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

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Attribute+%22AttributeFunction%22+cannot+target+Class+%28allowed+targets%3A+Function%29.html>`_



Connex PHP features
-------------------

  + `attribute <https://php-dictionary.readthedocs.io/en/latest/dictionary/attribute.ini.html>`_


Suggestions
___________

* Remove the attribute from the wrongly attributed structure
* Extend the configuration of the attribute with Attribute::TARGET_*




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/WrongAttributeConfiguration                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
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
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


