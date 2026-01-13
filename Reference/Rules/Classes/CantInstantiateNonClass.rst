.. _classes-cantinstantiatenonclass:

.. _cant-instantiate-non-class:

Cant Instantiate Non Class
++++++++++++++++++++++++++

  It is not possible to instantiate anything else than a class. Interfaces, enumerations and traits cannot be instantiated.

.. code-block:: php
   
   <?php
   
   class c {} 
   
   $object = new c;
   
   trait t {}
   new t;
   
   ?>
Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/+Cannot+instantiate+trait+t+.html>`_
  + `1 <https://php-errors.readthedocs.io/en/latest/messages/+Cannot+instantiate+interface+i+.html>`_
  + `2 <https://php-errors.readthedocs.io/en/latest/messages/+Cannot+instantiate+enum+e+.html>`_




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CantInstantiateNonClass                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


