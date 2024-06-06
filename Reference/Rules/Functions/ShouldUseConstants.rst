.. _functions-shoulduseconstants:

.. _should-use-existing-constants:

Should Use Existing Constants
+++++++++++++++++++++++++++++

  The following functions have related constants that should be used as arguments, instead of scalar literals, such as integers or strings.

.. code-block:: php
   
   <?php
   
   // The file is read and new lines are ignored.
   $lines = file('file.txt', FILE_IGNORE_NEW_LINES)
   
   // What is this doing, with 2 ? 
   $lines = file('file.txt', 2);
   
   ?>

See also `Bitmask Constant Arguments in PHP <https://medium.com/@liamhammett/bitmask-constant-arguments-in-php-cf32bf35c73>`_.


Suggestions
___________

* Use PHP native constants whenever possible, for better readability.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/ShouldUseConstants                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | predefined-constant, constant                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-tine20-functions-shoulduseconstants`                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


