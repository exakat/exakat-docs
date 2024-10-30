.. _functions-duplicatenamedparameter:

.. _duplicate-named-parameter:

Duplicate Named Parameter
+++++++++++++++++++++++++

  Two parameters have the same name in a method call. This will yield a Fatal `error <https://www.php.net/error>`_ at execution time.

.. code-block:: php
   
   <?php
   
   function foo($a, $b) {}
   
   // parameters are all distinct
   foo(a:1, b:2);
   
   // parameter a is double
   foo(a:1, a:1);
   
   ?>

See also `Function arguments <https://www.php.net/manual/en/functions.arguments.php>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Named+parameter+%24a+overwrites+previous+argument.html>`_



Connex PHP features
-------------------

  + `named-parameter <https://php-dictionary.readthedocs.io/en/latest/dictionary/named-parameter.ini.html>`_


Suggestions
___________

* Review the parameters names and remove the duplicates
* Review the parameters names and makes the names unique




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/DuplicateNamedParameter                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.3                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and older                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+


