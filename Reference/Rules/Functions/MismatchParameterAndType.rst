.. _functions-mismatchparameterandtype:

.. _mismatch-parameter-and-type:

Mismatch Parameter And Type
+++++++++++++++++++++++++++

.. meta::
	:description:
		Mismatch Parameter And Type: When the name of the parameter contradicts the type of the parameter.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Mismatch Parameter And Type
	:twitter:description: Mismatch Parameter And Type: When the name of the parameter contradicts the type of the parameter
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Mismatch Parameter And Type
	:og:type: article
	:og:description: When the name of the parameter contradicts the type of the parameter
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Mismatch Parameter And Type.html
	:og:locale: en
When the name of the parameter contradicts the type of the parameter.

This is mostly semantics, so it will affect the coder and the auditor of the code. PHP is immune to those errors.

.. code-block:: php
   
   <?php
   
   // There is a discrepancy between the typehint and the name of the variable
   function foo(int $string) { }
   
   // The parameter name is practising coding convention typehints
   function bar(int $int) { }
   
   ?>
Connex PHP features
-------------------

  + `parameter <https://php-dictionary.readthedocs.io/en/latest/dictionary/parameter.ini.html>`_
  + `type <https://php-dictionary.readthedocs.io/en/latest/dictionary/type.ini.html>`_
  + `semantics <https://php-dictionary.readthedocs.io/en/latest/dictionary/semantics.ini.html>`_


Suggestions
___________

* Synch the name of the parameter and the typehint.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/MismatchParameterAndType                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.8                                                                                                                   |
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


