.. _namespaces-usefunctionsconstants:

.. _use-const-and-functions:

Use Const And Functions
+++++++++++++++++++++++

.. meta\:\:
	:description:
		Use Const And Functions: Since PHP 5.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use Const And Functions
	:twitter:description: Use Const And Functions: Since PHP 5
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use Const And Functions
	:og:type: article
	:og:description: Since PHP 5
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Namespaces/UseFunctionsConstants.html
	:og:locale: en
  Since PHP 5.6 it is possible to import specific functions or constants from other namespaces.

.. code-block:: php
   
   <?php
   
   namespace A {
       const X = 1;
       function foo() { echo __FUNCTION__; }
   }
   
   namespace My{
       use function A\foo;
       use constant A\X;
   
       echo foo(X);
   }
   
   ?>

See also `Using namespaces: Aliasing/Importing <https://www.php.net/manual/en/language.namespaces.importing.php>`_.


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Namespaces/UseFunctionsConstants                                                                                                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.6 and more recent                                                                                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


