.. _dump-combinedcalls:

.. _combined-calls:

Combined Calls
++++++++++++++

  This collects all the combined function or method calls. Those are methods that are called in succession. 

.. code-block:: php
   
   <?php
   
   $a = ucfirst(strtolower($name));
   
   ?>

Specs
_____

+--------------+------------------------------------------------------+
| Short name   | Dump/CombinedCalls                                   |
+--------------+------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Dump <ruleset-Dump>` |
+--------------+------------------------------------------------------+
| Exakat since | 2.6.5                                                |
+--------------+------------------------------------------------------+
| PHP Version  | All                                                  |
+--------------+------------------------------------------------------+
| Severity     | Minor                                                |
+--------------+------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                      |
+--------------+------------------------------------------------------+
| Precision    | High                                                 |
+--------------+------------------------------------------------------+
| Available in |                                                      |
+--------------+------------------------------------------------------+


