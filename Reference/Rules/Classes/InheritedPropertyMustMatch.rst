.. _classes-inheritedpropertymustmatch:

.. _inherited-property-type-must-match:

Inherited Property Type Must Match
++++++++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Inherited Property Type Must Match: Properties that are inherited between classes must match.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Inherited Property Type Must Match
	:twitter:description: Inherited Property Type Must Match: Properties that are inherited between classes must match
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Inherited Property Type Must Match
	:og:type: article
	:og:description: Properties that are inherited between classes must match
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/InheritedPropertyMustMatch.html
	:og:locale: en
  Properties that are inherited between classes must match. 

This affect public and protected properties. Private properties are immune to this rule, as they actually are distinct properties.

.. code-block:: php
   
   <?php
   
   class A {
       private A $a;
       protected array $b;
       public $c;
   }
   
   class B extends A {
       private A $a;       // OK, as it is private
       protected int $b;   // type must match with the previous definition
       public $c;          // no type behaves just like a type : it must match too.
   }
   
   ?>

See also `Properties <https://www.php.net/manual/en/language.oop5.properties.php>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Type+of+b%3A%3A%24a+must+not+be+defined+%28as+in+class+a%29.html>`_
  + `1 <https://php-errors.readthedocs.io/en/latest/messages/Type+of+b%3A%3A%24a+must+be+array+%28as+in+class+a%29.html>`_



Connex PHP features
-------------------

  + `inheritance <https://php-dictionary.readthedocs.io/en/latest/dictionary/inheritance.ini.html>`_
  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Suggestions
___________

* Remove the definition in the child class
* Synchronize the definition of the property in the child class




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/InheritedPropertyMustMatch                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.2                                                                                                                                                                                                        |
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


