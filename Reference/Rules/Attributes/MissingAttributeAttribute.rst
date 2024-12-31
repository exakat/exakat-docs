.. _attributes-missingattributeattribute:

.. _missing-attribute-attribute:

Missing Attribute Attribute
+++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Missing Attribute Attribute: A class that servers as attribute, should have the attribute ``#[Attribute]``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Missing Attribute Attribute
	:twitter:description: Missing Attribute Attribute: A class that servers as attribute, should have the attribute ``#[Attribute]``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Missing Attribute Attribute
	:og:type: article
	:og:description: A class that servers as attribute, should have the attribute ``#[Attribute]``
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Attributes/MissingAttributeAttribute.html
	:og:locale: en
  A class that servers as `attribute <https://www.php.net/attribute>`_, should have the `attribute <https://www.php.net/attribute>`_ ``#[`Attribute <https://www.php.net/attribute>`_]``. 

While not strictly required, it is still recommended to create an actual class for every `attribute <https://www.php.net/attribute>`_.

.. code-block:: php
   
   <?php
   
   namespace Example;
   
   use Attribute;
   
   #[Attribute]
   class MyAttribute
   {
   }
   
   #Missing the above attribute
   class MyOtherAttribute
   {
   }
   
   ?>

See also `Declaring Attribute Classes <https://www.php.net/manual/en/language.attributes.classes.php>`_.

Connex PHP features
-------------------

  + `attribute <https://php-dictionary.readthedocs.io/en/latest/dictionary/attribute.ini.html>`_


Suggestions
___________

* Add the Attribute attribute to those classes




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Attributes/MissingAttributeAttribute                                                                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Attributes <ruleset-Attributes>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.4                                                                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


