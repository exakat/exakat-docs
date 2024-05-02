.. _functions-useconstantsasreturns:

.. _use-constants-as-returns:

Use Constants As Returns
++++++++++++++++++++++++

  When a native PHP function returns only constants, it is recommended to use those constants to identify the returned values.

.. code-block:: php
   
   <?php
   
   if (preg_last_error() != PREG_NO_ERROR ) {
       // An error occured with the last Regex call
   }
   
   // Who will guess PREG_JIT_STACKLIMIT_ERROR ? 
   if (preg_last_error() == 6 ) {
       // An error occured with the last Regex call
   }
   
   ?>

Suggestions
___________

* Use the valid constants to identify the results




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UseConstantsAsReturns                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


