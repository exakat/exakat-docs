.. _functions-wrongoptionalparameter:

.. _wrong-optional-parameter:

Wrong Optional Parameter
++++++++++++++++++++++++

  Wrong placement of optional parameters.

PHP parameters are optional when they defined with a default value, like this : 


.. code-block:: php
   
   <?php
       function x($arg = 1) {
           // PHP code here
       }
   ?>


When a function have both compulsory and optional parameters, the compulsory ones should appear first, and the optional should appear last : 


.. code-block:: php
   
   <?php
       function x($arg, $arg2 = 2) {
           // PHP code here
       }
   ?>


PHP solves this problem at runtime, assign values in the same other, but will miss some of the default values and emits warnings. 

It is better to put all the optional parameters at the end of the method's signature.

Optional parameter wrongly placed are now a Notice in PHP 8.0. The only previous case that is allowed in PHP 8.0 and also in this analysis, is when the ``null`` value is used as default for typed arguments.

See also `Function arguments <https://www.php.net/manual/en/functions.arguments.php>`_.


Suggestions
___________

* Give default values to all but first parameters. Null is a good default value, as PHP will use it if not told otherwise. 
* Remove default values to all but last parameters. That is probably a weak solution.
* Change the order of the values, so default-valued parameters are at the end. This will probably have impact on the rest of the code, as the API is changing.




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Functions/WrongOptionalParameter                                                                                                                                                                                                     |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                                                                                                                                  |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                                                                                                                      |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.1 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/.html>`__                                                                                                                                           |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                                                                            |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features         | parameter, optional-parameter                                                                                                                                                                                                        |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples         | :ref:`case-fuelcms-functions-wrongoptionalparameter`, :ref:`case-vanilla-functions-wrongoptionalparameter`                                                                                                                           |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


