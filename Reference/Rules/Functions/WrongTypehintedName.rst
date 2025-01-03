.. _functions-wrongtypehintedname:

.. _wrong-typehinted-name:

Wrong Typehinted Name
+++++++++++++++++++++

.. meta::
	:description:
		Wrong Typehinted Name: The parameter name doesn't reflect the typehint used.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Wrong Typehinted Name
	:twitter:description: Wrong Typehinted Name: The parameter name doesn't reflect the typehint used
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Wrong Typehinted Name
	:og:type: article
	:og:description: The parameter name doesn't reflect the typehint used
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Wrong Typehinted Name.html
	:og:locale: en
The parameter name doesn't reflect the typehint used.

There are no restriction on parameter names, except its uniqueness in the signature. Yet, using a scalar typehint as the name for another typehinted value is just misleading. 
This analysis relies on exact names : calling an array a list of ``strings`` is OK with this analysis.

This analysis relies on a few variations of names : ``bool`` and ``boolean``, ``int`` and ``integer``.

.. code-block:: php
   
   <?php
   
   function foo(string $array,
                int $int) {
       // doSomething()
   }
   
   function bar(array $strings) {
       // doSomething()
   }
   
   ?>
Connex PHP features
-------------------

  + `type <https://php-dictionary.readthedocs.io/en/latest/dictionary/type.ini.html>`_


Suggestions
___________

* Rename the parameter




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/WrongTypehintedName                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Coding conventions <ruleset-Coding-conventions>`, :ref:`Semantics <ruleset-Semantics>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.2                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


