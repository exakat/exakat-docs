.. _functions-badtypehintrelay:

.. _bad-type-relay:

Bad Type Relay
++++++++++++++

  A bad type relay happens where a types argument is relayed to a parameter with another type. This leads to a Fatal `error <https://www.php.net/error>`_, and stops execution. This is possibly a piece of dead code.

It is recommended to harmonize the types, so the two methods are compatible.

.. code-block:: php
   
   <?php
   
   // the $i argument is relayed to bar, which is expecting a string. 
   function foo(int $i) : string {
       return bar($i);
   }
   
   // the return value for the bar function is not compatible with the one from foo;
   function bar(string $s) : int {
       return (int) $string + 1;
   }
   
   ?>
Connex PHP features
-------------------

  + `type <https://php-dictionary.readthedocs.io/en/latest/dictionary/type.ini.html>`_


Suggestions
___________

* Harmonize the type so they match one with the other.
* Remove dead code
* Apply type casting before calling the next function, or return value




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/BadTypehintRelay                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Typechecks <ruleset-Typechecks>`                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.6                                                                                                                   |
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


