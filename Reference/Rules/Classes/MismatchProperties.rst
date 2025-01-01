.. _classes-mismatchproperties:

.. _mismatch-properties-typehints:

Mismatch Properties Typehints
+++++++++++++++++++++++++++++

.. meta::
	:description:
		Mismatch Properties Typehints: Properties must match within the same family.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Mismatch Properties Typehints
	:twitter:description: Mismatch Properties Typehints: Properties must match within the same family
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Mismatch Properties Typehints
	:og:type: article
	:og:description: Properties must match within the same family
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/MismatchProperties.html
	:og:locale: en
Properties must match within the same family.

When a property is declared both in a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class, and a child class, they must have the same type. The same type includes a possible null value.

This doesn't apply to private properties, which are only visible locally.
This code will lint, but not execute.

.. code-block:: php
   
   <?php
   
   // property $p is declared as an object of type a
   class x { 
       protected A $p; 
   }
   
   // property $p is declared again, this time without a type
   class a extends x { 
       protected $p; 
   }
   ?>
Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Type+of+b%3A%3A%24b+must+be+A+%28as+in+class+a%29.html>`_



Connex PHP features
-------------------

  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Suggestions
___________

* Remove some of the property declarations, and only keep it in the highest ranking parent
* Match the typehints of the property declarations
* Make the properties private
* Remove the child class (or the parent class)




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MismatchProperties                                                                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.4                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


