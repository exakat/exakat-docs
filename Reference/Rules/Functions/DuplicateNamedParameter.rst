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


Suggestions
___________

* Review the parameters names and remove the duplicates
* Review the parameters names and makes the names unique




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/DuplicateNamedParameter                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`LintButWontExec <ruleset-LintButWontExec>`            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | named-parameter                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


