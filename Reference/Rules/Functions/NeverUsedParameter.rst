.. _functions-neverusedparameter:

.. _never-called-parameter:

Never Called Parameter
++++++++++++++++++++++

  When a parameter is never used at calltime. It always falls back to its default value : then, it may be turned into a local variable.

Parameter without a default value are reported by PHP, and are usually always filled. 


.. code-block:: php
   
   <?php
   
   // $b may be turned into a local var, it is unused
   function foo($a, $b = 1) {
       return $a + $b;
   }
   
   // whenever foo is called, the 2nd arg is not mentioned
   foo($a);
   foo(3);
   foo('a');
   foo($c);
   
   ?>


This analysis checks for actual usage of the parameter, from the outside of the method. This is different from checking if the parameter is used inside the method.

See also :ref:`Unused Parameter <unused-parameter>`, :ref:`Cancelled Parameter <cancelled-parameter>` and :ref:`Parameter Hiding <parameter-hiding>`.


Suggestions
___________

* Drop the unused argument in the method definition
* Actually use the argument when calling the method
* Drop the default value, and check warnings that mention usage of this parameter




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/NeverUsedParameter                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Rector <ruleset-Rector>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.6                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-piwigo-functions-neverusedparameter`                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


