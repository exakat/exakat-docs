.. _traits-traitisnotatype:

.. _trait-is-not-a-type:

Trait Is Not A Type
+++++++++++++++++++

.. meta::
	:description:
		Trait Is Not A Type: A trait cannot be used for typing.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Trait Is Not A Type
	:twitter:description: Trait Is Not A Type: A trait cannot be used for typing
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Trait Is Not A Type
	:og:type: article
	:og:description: A trait cannot be used for typing
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Trait Is Not A Type.html
	:og:locale: en
A trait cannot be used for typing. It is used by a classes, and those classes should be used for typing.

.. code-block:: php
   
   <?php
   
   trait t {}
   
   // No way to provide an object of type t
   function foo(t $t) {
   
   }
   
   ?>

Suggestions
___________

* Use the classes that use the trait as type
* Provide an interface that matches the trait, and make the using classes implements it too




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/TraitIsNotAType                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.2                                                                                                                   |
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


