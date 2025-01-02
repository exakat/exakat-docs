.. _classes-coulduseclassoperator:

.. _could-use-class-operator:

Could Use Class Operator
++++++++++++++++++++++++

.. meta::
	:description:
		Could Use Class Operator: The class operator is `::class`.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Use Class Operator
	:twitter:description: Could Use Class Operator: The class operator is `::class`
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Use Class Operator
	:og:type: article
	:og:description: The class operator is `::class`
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Use Class Operator.html
	:og:locale: en
The class operator is `\:\:class`. With a class name as left operator, it provides the full class name. 

Classes may also be identified with a string, as a fully qualified name. Using the class operator is a more explicit way to do it.

The `\:\:class` operator works with the local use expressions. It also provides a string, which may be further processed.
The class operator is also called the 'scope resolution operator'.

.. code-block:: php
   
   <?php
   
   use A\B\C;
   
   $a = C::class;
   $a = \A\B\C::class; // also valid
   $object = new $a(); // object of A\B\C.
   
   // string version
   $a = '\a\b\c';
   $object = new $a(); // object of A\B\C.
   
   ?>

See also `Scope Resolution Operator (::) <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_.

Connex PHP features
-------------------

  + `class-operator <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-operator.ini.html>`_


Suggestions
___________

* Replace the string with the class operator




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldUseClassOperator                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


