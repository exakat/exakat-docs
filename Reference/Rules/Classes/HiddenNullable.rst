.. _classes-hiddennullable:

.. _implicit-nullable-type:

Implicit Nullable Type
++++++++++++++++++++++

.. meta::
	:description:
		Implicit Nullable Type: Argument with default value of null are nullable.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Implicit Nullable Type
	:twitter:description: Implicit Nullable Type: Argument with default value of null are nullable
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Implicit Nullable Type
	:og:type: article
	:og:description: Argument with default value of null are nullable
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Implicit Nullable Type.html
	:og:locale: en
Argument with default value of null are nullable. It works both with the ``null`` typehint (PHP 8.0), or the ``?`` operator are not used, setting the default value to null is allowed, and makes the argument nullable.

This works with single types, both classes and scalars; it works with union types but not with intersection types. 

This doesn't happen with properties : they must be defined with the nullable type to accept a ``null``value as default value.

This doesn't happen with constant, whose value must be explicitely defined. 

In PHP 8.4, the implicit nullable type are deprecated. They might be removed in PHP 9.0.


.. code-block:: php
   
   <?php
   
   // explicit nullable parameter $s
   function bar(?string $s = null) {
   
   // implicit nullable parameter $s
   function foo(string $s = null) {
       echo $s ?? 'NULL-value';
   }
   
   // both display NULL-value
   foo(); 
   foo(null);
   
   ?>

See also `Nullable types <https://wiki.php.net/rfc/nullable_types>`_, `Type declaration <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration>`_, `Deprecate implicit nullable parameters #3535 <https://github.com/php/php-src/pull/3535>`_ and `PHP RFC: Deprecate implicitly nullable parameter types <https://wiki.php.net/rfc/deprecate-implicitly-nullable-types>`_.

Connex PHP features
-------------------

  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_
  + `nullable <https://php-dictionary.readthedocs.io/en/latest/dictionary/nullable.ini.html>`_


Suggestions
___________

* Change the default value to a compatible literal : for example, ``string $s = ''``
* Add the explicit ``?`` nullable operator, or ``null``with PHP 8.0
* Remove the default value




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/HiddenNullable                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.0                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


