.. _traits-usedtrait:

.. _used-trait:

Used Trait
++++++++++

.. meta::
	:description:
		Used Trait: This rule marks a trait as being used by a class or another trait.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Used Trait
	:twitter:description: Used Trait: This rule marks a trait as being used by a class or another trait
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Used Trait
	:og:type: article
	:og:description: This rule marks a trait as being used by a class or another trait
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Used Trait.html
	:og:locale: en
This rule marks a trait as being used by a class or another trait. 

Traits are used with the ``use`` keyword inside traits, classes and enumerations. 

This is a base rule to extract unused traits from the code. 

.. code-block:: php
   
   <?php
   
   // One used trait
   trait usedTrait {}
   
   // One unused trait
   trait unusedTrait {}
   
   class foo {
       use usedTrait; 
   }
   
   ?>

See also `Traits <https://www.php.net/manual/en/language.oop5.traits.php>`_.

Connex PHP features
-------------------

  + `trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/UsedTrait                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


