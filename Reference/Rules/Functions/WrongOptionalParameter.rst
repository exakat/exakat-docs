.. _functions-wrongoptionalparameter:

.. _wrong-optional-parameter:

Wrong Optional Parameter
++++++++++++++++++++++++

  Wrong placement of optional parameters.

PHP parameters are optional when they defined with a default value, like this : 

When a function have both compulsory and optional parameters, the compulsory ones should appear first, and the optional should appear last : 

PHP solves this problem at runtime, assign values in the same other, but will miss some of the default values and emits warnings. 

It is better to put all the optional parameters at the end of the method's signature.

Optional parameter wrongly placed are now a Notice in PHP 8.0. The only previous case that is allowed in PHP 8.0 and also in this analysis, is when the ``null`` value is used as default for typed arguments.

.. code-block:: php
   
   <?php
       function x($arg = 1) {
           // PHP code here
       }
   ?>

See also `Function arguments <https://www.php.net/manual/en/functions.arguments.php>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Too+few+arguments+to+function+foo%28%29%2C+1+passed+and+exactly+2+expected.html>`_
  + `1 <https://php-errors.readthedocs.io/en/latest/messages/Deprecated%3A+Required+parameter+%24y+follows+optional+parameter+%24x.html>`_
  + `2 <https://php-errors.readthedocs.io/en/latest/messages/Optional+parameter+%24a+declared+before+required+parameter+%24b+is+implicitly+treated+as+a+required+parameter.html>`_



Connex PHP features
-------------------

  + `parameter <https://php-dictionary.readthedocs.io/en/latest/dictionary/parameter.ini.html>`_
  + `optional-parameter <https://php-dictionary.readthedocs.io/en/latest/dictionary/optional-parameter.ini.html>`_


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
| PHP Version      | With PHP 8.0 and older                                                                                                                                                                                                               |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                                                                                                                      |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.1 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/.html>`__                                                                                                                                           |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                                                                            |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples         | :ref:`case-fuelcms-functions-wrongoptionalparameter`, :ref:`case-vanilla-functions-wrongoptionalparameter`                                                                                                                           |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


