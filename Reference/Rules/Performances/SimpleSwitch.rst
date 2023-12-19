.. _performances-simpleswitch:

.. _simple-switch-and-match:

Simple Switch And Match
+++++++++++++++++++++++

  `Switch() <https://www.php.net/manual/en/control-structures.switch.php>`_ and `match() <https://www.php.net/manual/en/control-structures.match.php>`_ are faster when relying only on literal integers or strings.

Since PHP 7.2, simple switches, that use only literal strings or integers, are optimized. The bigger the switch, the greater the gain.
`Match() <https://www.php.net/manual/en/control-structures.match.php>`_ was introduced in PHP 8.0

In particular, this optimisation doesn't work with any expressions (constant or not), function call, methodcall, constant usage, etc. Only literal values, string or integer.

When the switch is partially build of literals, it is worth splitting the switch in two : first level, only with the literal cases, and, in the default, the dynamic values. This brings some performances, though it is a micro-optimisation. 


.. code-block:: php
   
   <?php
   
   // Optimized switch. 
   switch($b) {
       case "a":
           break;
       case "b":
           break;
       case "c":
           break;
       case "d":
           break;
       default :
           break;
   }
   
   // Unoptimized switch. 
   // Try moving the foo() call in the default, to keep the rest of the switch optimized.
   switch($c) {
       case "a":
           break;
       case foo($b):
           break;
       case C:
           break;
       case "c":
           break;
       case "d":
           break;
       default :
           break;
   }
   
   // Partially optimised switch
   // Try moving the foo() call in the default, to keep the rest of the switch optimized.
   switch($c) {
       case "a":
           break;
       case "c":
           break;
       case "d":
           break;
       default :
           switch($c) {
               case foo($b):
               break;
   
               case C:
               break;
   
           default :
               break;
           }
           break;
   }
   
   ?>

See also `PHP 7.2's "switch" optimisations <https://derickrethans.nl/php7.2-switch.html>`_.


Suggestions
___________

* Split the switch between literal and dynamic cases
* Remove the dynamic cases from the switch
* Move the most common case to the beginning of the switch




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/SimpleSwitch                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Performances <ruleset-Performances>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.2 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | switch, match                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


