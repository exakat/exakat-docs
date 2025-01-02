.. _functions-missingtypehint:

.. _missing-typehint:

Missing Typehint
++++++++++++++++

.. meta::
	:description:
		Missing Typehint: No typehint was found for a parameter, a return type for a method or a property.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Missing Typehint
	:twitter:description: Missing Typehint: No typehint was found for a parameter, a return type for a method or a property
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Missing Typehint
	:og:type: article
	:og:description: No typehint was found for a parameter, a return type for a method or a property
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Missing Typehint.html
	:og:locale: en
No typehint was found for a parameter, a return type for a method or a property.

void is considered a specified typehint, and is not reported here.

.. code-block:: php
   
   <?php
   
   class x {
       private $no_property;
       
       function foo($no_typehint) : void {}
   
       function no_return_type() {}
   }
   ?>

See also `Type Declaration <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration>`_.

Connex PHP features
-------------------

  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_


Suggestions
___________

* Add a type to the argument, property or method




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/MissingTypehint                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Typechecks <ruleset-Typechecks>`    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.5                                                                                                                   |
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


