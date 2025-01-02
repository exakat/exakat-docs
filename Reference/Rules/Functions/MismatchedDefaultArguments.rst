.. _functions-mismatcheddefaultarguments:

.. _mismatched-default-arguments:

Mismatched Default Arguments
++++++++++++++++++++++++++++

.. meta::
	:description:
		Mismatched Default Arguments: Arguments are relayed from one method to the other, and the arguments have different default values.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Mismatched Default Arguments
	:twitter:description: Mismatched Default Arguments: Arguments are relayed from one method to the other, and the arguments have different default values
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Mismatched Default Arguments
	:og:type: article
	:og:description: Arguments are relayed from one method to the other, and the arguments have different default values
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Mismatched Default Arguments.html
	:og:locale: en
Arguments are relayed from one method to the other, and the arguments have different default values. 

Although it is possible to have different default values, it is worth checking why this is actually the case.
This analysis reports the original arguments. Starting from it, follow the usage of the argument in its method, and find calls to other methods. 

This analysis omits reporting argument when one of them does not have a default value.

.. code-block:: php
   
   <?php
   
   function foo($a = null, $b = array() ) {
       // foo method calls directly bar. 
       // When argument are provided, it's OK
       // When argument are omited, the default value is not the same as the next method
       bar($a, $b);
   }
   
   function bar($c = 1, $d = array() ) {
   
   }
   
   ?>
Connex PHP features
-------------------

  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_
  + `parameter <https://php-dictionary.readthedocs.io/en/latest/dictionary/parameter.ini.html>`_


Suggestions
___________

* Synchronize default values to avoid surprises
* Drop some of the default values




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/MismatchedDefaultArguments                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Typechecks <ruleset-Typechecks>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.3                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-spip-functions-mismatcheddefaultarguments`                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+


