.. _classes-implementisforinterface:

.. _implements-is-for-interface:

Implements Is For Interface
+++++++++++++++++++++++++++

  With class heritage, implements should be used for interfaces, and extends with classes.

PHP defers the implements check until execution : the code in example does lint, but won,t run.

.. code-block:: php
   
   <?php
   
   class x {
       function foo() {}
   }
   
   interface y {
       function foo();
   }
   
   // Use implements with an interface
   class z implements y {}
   
   // Implements is for an interface, not a class
   class z implements x {}
   
   ?>
Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/b+cannot+implement+a+-+it+is+not+an+interface.html>`_



Connex PHP features
-------------------

  + `implements <https://php-dictionary.readthedocs.io/en/latest/dictionary/implements.ini.html>`_
  + `interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/interface.ini.html>`_


Suggestions
___________

* Create an interface from the class, and use it with the implements keyword




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ImplementIsForInterface                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
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


