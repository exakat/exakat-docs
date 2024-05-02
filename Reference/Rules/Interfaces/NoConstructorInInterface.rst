.. _interfaces-noconstructorininterface:

.. _no-constructor-in-interface:

No Constructor In Interface
+++++++++++++++++++++++++++

  PHP manual recommends not adding constructors to interfaces. 

'Although they are supported, including constructors in interfaces is strongly discouraged. Doing so significantly reduces the flexibility of the object implementing the interface. Additionally, constructors are not enforced by inheritance rules, which can cause inconsistent and unexpected behavior.'

```

```

.. code-block:: php
   
   <?php
   
   interface with {
       function __construct();
   }
   
   ?>

See also `Object Interfaces <https://www.php.net/manual/en/language.oop5.interfaces.php>`_.


Suggestions
___________

* Remove the constructor from the interface




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/NoConstructorInInterface                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.0                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------+
| Features     | interface                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------+


