.. _structures-impliedif:

.. _implied-if:

Implied If
++++++++++

  It is confusing to emulate if/then with boolean operators.

It is possible to emulate a if/then structure by using the operators 'and' and 'or'. Since optimizations will be applied to them : 
when the left operand of 'and' is false, the right one is not executed, as its `result <https://www.php.net/result>`_ is useless; 
when the left operand of 'or' is true, the right one is not executed, as its `result <https://www.php.net/result>`_ is useless; 

However, such structures are confusing. It is easy to misread them as conditions, and ignore an important logic step. 


.. code-block:: php
   
   <?php
   
   // Either connect, or die
   mysql_connect('localhost', $user, $pass) or die();
   
   // Defines a constant if not found. 
   defined('SOME_CONSTANT') and define('SOME_CONSTANT', 1);
   
   // Defines a default value if provided is empty-ish 
   // Warning : this is 
   $user = $_GET['user'] || 'anonymous';
   
   ?>


It is recommended to use a real 'if then' structures, to make the condition readable.

Suggestions
___________

* Replace this expression by an explicit if-then structure




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ImpliedIf                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Rector <ruleset-Rector>`                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-implied-if <https://github.com/dseguy/clearPHP/tree/master/rules/no-implied-if.md>`__                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


