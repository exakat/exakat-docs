.. _functions-variableparameterambiguityinarrowfunction:

.. _variable-parameter-ambiguity-in-arrow-function:

Variable Parameter Ambiguity In Arrow Function
++++++++++++++++++++++++++++++++++++++++++++++

  Avoid using a parameter that is also the name of a local variable.

Arrow functions import automatically the variables from the local context in their body. Yet, a variable name may also be used as the name of a parameter. In that case, PHP use the parameter, and omits the value of the local variable.

.. code-block:: php
   
   <?php
   
   // $b is a parameter, $a is a local variable
   $a = 1;
   fn($b) => $a + $b;
   
   //  $a is a local variable, but also a parameter.
   // PHP uses the parameter, and omits the local variable
   fn($a) => $a + 1;
   
   ?>

Suggestions
___________

* Use parameter names that are distinct from the local variables names.




Specs
_____

+--------------+------------------------------------------------------------------------------+
| Short name   | Functions/VariableParameterAmbiguityInArrowFunction                          |
+--------------+------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>` |
+--------------+------------------------------------------------------------------------------+
| Exakat since | 2.6.6                                                                        |
+--------------+------------------------------------------------------------------------------+
| PHP Version  | All                                                                          |
+--------------+------------------------------------------------------------------------------+
| Severity     | Minor                                                                        |
+--------------+------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                              |
+--------------+------------------------------------------------------------------------------+
| Precision    | Very high                                                                    |
+--------------+------------------------------------------------------------------------------+
| Features     | arrow-function                                                               |
+--------------+------------------------------------------------------------------------------+
| Available in |                                                                              |
+--------------+------------------------------------------------------------------------------+


