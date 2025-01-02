.. _classes-nonppp:

.. _forgotten-visibility:

Forgotten Visibility
++++++++++++++++++++

.. meta::
	:description:
		Forgotten Visibility: Some classes elements (property, method, constant) are missing their explicit visibility.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Forgotten Visibility
	:twitter:description: Forgotten Visibility: Some classes elements (property, method, constant) are missing their explicit visibility
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Forgotten Visibility
	:og:type: article
	:og:description: Some classes elements (property, method, constant) are missing their explicit visibility
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Forgotten Visibility.html
	:og:locale: en
Some classes elements (property, method, constant) are missing their explicit visibility.

By default, it is public. It should at least be mentioned as public, or may be reviewed as protected or private. 

Class constants support also visibility since PHP 7.1.

final, `static <https://www.php.net/manual/en/language.oop5.static.php>`_ and abstract are not counted as visibility. Only public, private and protected. The PHP 4 var keyword is counted as undefined.

Traits, classes and interfaces are checked.

.. code-block:: php
   
   <?php
   
   // Explicit visibility
   class X {
       protected sconst NO_VISIBILITY_CONST = 1; // For PHP 7.2 and later
   
       private $noVisibilityProperty = 2; 
       
       public function Method() {}
   }
   
   // Missing visibility
   class X {
       const NO_VISIBILITY_CONST = 1; // For PHP 7.2 and later
   
       var $noVisibilityProperty = 2; // Only with var
       
       function NoVisibilityForMethod() {}
   }
   
   ?>

See also `Visibility <https://www.php.net/manual/en/language.oop5.visibility.php>`_ and `Understanding The Concept Of Visibility In Object Oriented PHP <https://torquemag.io/2016/05/understanding-concept-visibility-object-oriented-php/>`_.

Connex PHP features
-------------------

  + `visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/visibility.ini.html>`_


Suggestions
___________

* Always add explicit visibility to methods and constants in a class
* Always add explicit visibility to properties in a class, after PHP 7.4




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/NonPpp                                                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `always-have-visibility <https://github.com/dseguy/clearPHP/tree/master/rules/always-have-visibility.md>`__                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-fuelcms-classes-nonppp`, :ref:`case-livezilla-classes-nonppp`                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


