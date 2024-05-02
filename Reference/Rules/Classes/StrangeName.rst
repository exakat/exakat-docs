.. _classes-strangename:

.. _strange-names-in-classes:

Strange Names In Classes
++++++++++++++++++++++++

  Those methods, properties, constants or types should have another name.

Ever wondered why the ``__constructor`` is never called? Or the ``__consturct`` ? 

Those errors most often originate from typos, or quick fixes that where not fully tested. Other times, they were badly chosen, or ran into PHP's own reserved keywords.

.. code-block:: php
   
   <?php
   
   class foo {
       // The real constructor
       function __construct() {}
   
       // The fake constructor
       function __constructor() {}
       
       // The 'typo'ed' constructor
       function __consturct() {}
       
       // This doesn't clone
       function clone() {}
   }
   
   ?>

Suggestions
___________

* Use the proper name
* Remove the method, when it is not used and tests still pass.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/StrangeName                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Semantics <ruleset-Semantics>`                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.1                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


