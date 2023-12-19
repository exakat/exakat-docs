.. _functions-unusedfunctions:

.. _unused-functions:

Unused Functions
++++++++++++++++

  The functions below are unused. They look like dead code.

Recursive functions, level 1, are detected : they are only reported when a call from outside the function is made. Recursive functions calls of higher level (A calls B calls A) are not handled.


.. code-block:: php
   
   <?php
   
   function used() {}
   // The 'unused' function is defined but never called
   function unused() {}
   
   // The 'used' function is called at least once
   used();
   
   ?>

Suggestions
___________

* Use the function in the code
* Remove the functions from the code




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UnusedFunctions                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Dead code <ruleset-Dead-code>`                                                          |
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
| Features     | function, unused                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-woocommerce-functions-unusedfunctions`, :ref:`case-piwigo-functions-unusedfunctions`                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


