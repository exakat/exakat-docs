.. _functions-neverusedparameter:

.. _never-called-parameter:

Never Called Parameter
++++++++++++++++++++++

  This analysis reports when a parameter is never used at calltime. 

Such parameter has a default value, and always falls back to it. As such, it may be turned into a local variable.

A never called parameter is often planned for future use, though, so far, the code base doesn't make use of it. It also happens that the code use it, but is not part of the analyzed code base, such as a plugin system.

This issue is silent: it doesn't yield any `error <https://www.php.net/error>`_. It is also difficult to identify, as it requires checking all the usage of the method.

This analysis checks for actual usage of the parameter, from the outside of the method. This is different from checking if the parameter is used inside the method.


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

See also :ref:`Unused Parameter <unused-parameter>`, :ref:`Cancelled Parameter <cancelled-parameter>` and :ref:`Parameter Hiding <parameter-hiding>`.

Connex PHP features
-------------------

  + `silent <https://php-dictionary.readthedocs.io/en/latest/dictionary/silent.ini.html>`_


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
| Related rule | :ref:`could-be-class-constant`, :ref:`unused-parameter`                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


