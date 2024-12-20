.. _functions-mismatcheddefaultarguments:

.. _mismatched-default-arguments:

Mismatched Default Arguments
++++++++++++++++++++++++++++

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


