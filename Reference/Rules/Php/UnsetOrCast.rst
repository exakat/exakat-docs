.. _php-unsetorcast:

.. _unset()-or-(unset):

Unset() Or (unset)
++++++++++++++++++

  Unset() and (unset) have the same functional use. 

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make them all the same. 

It happens that unset() or (unset) are used depending on coding style and files. One file may be consistently using unset(), while the others are all using (unset). 

In PHP 8.0, the cast ``(unset)`` is not available anymore. It is recomended to avoid using it.

.. code-block:: php
   
   <?php
   
   // be consistent
   (unset) $a1;
   (unset) $a2;
   (unset) $a3;
   (unset) $a4;
   (unset) $a5;
   (unset) $a6;
   (unset) $a7;
   (unset) $a8;
   (unset) $a9;
   (unset) $a10;
   (unset) $a11;
   (unset) $a12;
   
   unset($b);
   ?>

Suggestions
___________

* Use the correct parameter name
* Remove all the parameter names from the call
* Create a relay function with the correct parameter names




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UnsetOrCast                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Preferences <ruleset-Preferences>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | unset                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


