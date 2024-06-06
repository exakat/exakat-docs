.. _namespaces-overloadexistingnames:

.. _overload-existing-names:

Overload Existing Names
+++++++++++++++++++++++

  Imported alias have precedence over existing ones, and as such, may replace existing features with unexpected ones. 

This example shows how to replace `strtolower() <https://www.php.net/strtolower>`_ with `strtoupper() <https://www.php.net/strtoupper>`_ while keeping the main code intact. This might be very confusing code. 
This behavior is important for backward compatibility, and also to avoid naming conflicts when the coding has been done with a PHP installation which do not have some specific declaration. For example, a source may define an 'Event' class, which will be in conflict when the ext/event library is installed. 

This feature is also useful to mock some native PHP structures, during tests. 

This rule relies on the PDFF configuration to check for external existing structures.

.. code-block:: php
   
   <?php
   
   // Replacing a PHP classic with another one
   use function strtoupper as strtolower;
   
   echo strtolower('pHp'); 
   // displays PHP
   
   ?>

Suggestions
___________

* Use another local name than the general name
* Always code in a namespace to avoid conflict




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Namespaces/OverloadExistingNames                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.2                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | use-alias                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


