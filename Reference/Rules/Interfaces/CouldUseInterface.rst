.. _interfaces-coulduseinterface:

.. _forgotten-interface:

Forgotten Interface
+++++++++++++++++++

  The following classes have been found implementing an interface's methods, though it doesn't explicitly implements this interface. This may have been forgotten.

.. code-block:: php
   
   <?php
   
   interface i {
       function i(); 
   }
   
   // i is not implemented and declared
   class foo {
       function i() {}
       function j() {}
   }
   
   // i is implemented and declared
   class foo implements i {
       function i() {}
       function j() {}
   }
   
   ?>

See also :ref:`Could Use Trait <could-use-trait>`.


Suggestions
___________

* Mention interfaces explicitly whenever possible




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/CouldUseInterface                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.7                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | interface, ducktyping                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


