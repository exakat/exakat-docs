.. _structures-reusevariable:

.. _reuse-existing-variable:

Reuse Existing Variable
+++++++++++++++++++++++

  A variable is already holding the content that is calculated again : it could be used again. 

It is recommended to use the cached value. This saves some computation, in particular when used in a loop, and speeds up the process. This is called memoization.
Some expressions are not idempotent, and should not be cached. For example, calls to `time() <https://www.php.net/time>`_ or `fgets() <https://www.php.net/fgets>`_ return different values with the same parameters.

This may be a micro-optimisation.

.. code-block:: php
   
   <?php
   
   function foo($a) {
       $b = strtolower($a);
       
       // strtolower($a) is already calculated in $b. Just reuse the value.
       if (strtolower($a) === 'c') {
           doSomething();
       }
   }
   
   ?>

Suggestions
___________

* Reuse the existing variable




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ReuseVariable                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | memoization                                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


