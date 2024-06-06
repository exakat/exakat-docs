.. _classes-methodisoverwritten:

.. _method-is-overwritten:

Method Is Overwritten
+++++++++++++++++++++

  This rule marks a method that is overwritten in a child class. 

Any child that overwrite the method make that method reported here: the `result <https://www.php.net/result>`_ may be partial. 

This rule may lead to the usage of the ``Override`` `attribute <https://www.php.net/attribute>`_.


.. code-block:: php
   
   <?php
   
   class A {
       function intactMethodA() {}         // Not overwritten in any children
       function overwrittenMethodInAA() {} // overwritten in AA
   }
   
   class AA extends A {
       function intactMethodAA() {}        // Not overwritten, because no extends
       function overwrittenMethodInAA() {} // Not overwritten, because no extends
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MethodIsOverwritten                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.9                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | inheritance, override                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


