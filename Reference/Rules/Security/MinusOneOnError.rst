.. _security-minusoneonerror:

.. _minus-one-on-error:

Minus One On Error
++++++++++++++++++

  Some PHP native functions return -1 on `error <https://www.php.net/error>`_. They also return 1 in case of success, and 0 in case of failure. This leads to confusions.

In case the native function is used as a condition without explicit comparison, PHP type cast the return value to a boolean. In this case, -1 and 1 are both converted to true, and the condition applies. This means that an `error <https://www.php.net/error>`_ situation is mistaken for a successful event. 


.. code-block:: php
   
   <?php
   
   // Proper check of the return value
   if (openssl_verify($data, $signature, $public) === 1) {
       $this->loginAsUser($user);
   }
   
   // if this call fails, it returns -1, and is confused with true
   if (openssl_verify($data, $signature, $public)) {
       $this->loginAsUser($user);
   }
   ?>


This analysis searches for if/then structures, ternary operators inside `while() <https://www.php.net/manual/en/control-structures.while.php>`_ / do...`while() <https://www.php.net/manual/en/control-structures.while.php>`_ loops.

See also `Can you spot the vulnerability? (openssl_verify) <https://twitter.com/ripstech/status/1124325237967994880>`_ and `Incorrect Signature Verification <https://snyk.io/vuln/SNYK-PHP-SIMPLESAMLPHPSIMPLESAMLPHPMODULEINFOCARD-70167>`_.


Suggestions
___________

* Compare explicitly the return value to 1




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/MinusOneOnError                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Security <ruleset-Security>`                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


