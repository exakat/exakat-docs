.. _functions-relayfunction:

.. _relay-function:

Relay Function
++++++++++++++

  Relay function only delegates workload to another one. 

Relay functions and methods are delegating the actual work to another function or method. They do not have any impact on the results, besides exposing another name for the same feature.


.. code-block:: php
   
   <?php
   
   function myStrtolower($string) {
       return \strtolower($string);
   }
   
   ?>


Relay functions are typical of transition API, where an old API have to be preserved until it is fully migrated. Then, they may be removed, so as to reduce confusion, and simplify the API.

Suggestions
___________

* Remove relay function, call directly the final function
* Remove the target function, and move the code here
* Add more logic to that function, like conditions or cache




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/RelayFunction                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | function                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-teampass-functions-relayfunction`, :ref:`case-spip-functions-relayfunction`                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


