.. _php-onlyvariablepassedbyreference:

.. _only-variable-passed-by-reference:

Only Variable Passed By Reference
+++++++++++++++++++++++++++++++++

  Some methods require a variable as argument. Those arguments are passed by reference, and they must operate on a variable, or any data container (property, array element). 

This means that literal values, constants cannot be used as argument. This is also the case of literal values, returned by other methods.

This is also the case of ``isset()``, althought with a different `error <https://www.php.net/error>`_ message.

.. code-block:: php
   
   <?php
   
   echo end([1,2,3]);
   
   function foo() {
   	return [4,5,6];
   }
   
   echo end(foo());
   
   ?>
Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Argument+%231+%28%24array%29+could+not+be+passed+by+reference.html>`_
  + `1 <https://php-errors.readthedocs.io/en/latest/messages/Argument+%231+%28%24array%29+cannot+be+passed+by+reference.html>`_
  + `2 <https://php-errors.readthedocs.io/en/latest/messages/Cannot+use+isset%28%29+on+the+result+of+an+expression+%28you+can+use+%22null+%21%3D%3D+expression%22+instead%29.html>`_




Suggestions
___________

* Put the value in a variable before using it with the function.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/OnlyVariablePassedByReference                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+


