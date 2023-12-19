.. _functions-aliasesusage:

.. _native-alias-functions-usage:

Native Alias Functions Usage
++++++++++++++++++++++++++++

  PHP manual recommends to avoid function aliases.

Some PHP native functions have several names, and both may be used the same way. However, one of the names is the main name, and the others are aliases. Aliases may be removed or change or dropped in the future. Even if this is not forecast, it is good practice to use the main name, instead of the aliases. 


.. code-block:: php
   
   <?php
   
   // official way to count an array
   $n = count($array);
   
   // official way to count an array
   $n = sizeof($array);
   
   ?>


Aliases are compiled in PHP, and do not provide any performances over the normal function. 

Aliases are more likely to be removed later, but they have been around for a long time.

See also `List of function aliases <https://www.php.net/manual/en/aliases.php>`_.


Suggestions
___________

* Always use PHP recommended functions




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/AliasesUsage                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | native                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-aliases <https://github.com/dseguy/clearPHP/tree/master/rules/no-aliases.md>`__                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-cleverstyle-functions-aliasesusage`, :ref:`case-phpmyadmin-functions-aliasesusage`                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


