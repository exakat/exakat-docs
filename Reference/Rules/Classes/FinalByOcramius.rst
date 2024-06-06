.. _classes-finalbyocramius:

.. _class-should-be-final-by-ocramius:

Class Should Be Final By Ocramius
+++++++++++++++++++++++++++++++++

  'Make your classes always final, if they implement an interface, and no other public methods are defined'.

When a class should be final, as explained by ``Ocramius`` (``Marco Pivetta``).

.. code-block:: php
   
   <?php
   
   interface i1 {
       function i1() ;
   }
   
   // Class should final, as its public methods are in an interface
   class finalClass implements i1 {
       // public interface 
       function i1 () {}
       
       // private method
       private function a1 () {}
   }
   
   ?>

See also `Final classes by default, why? <https://matthiasnoback.nl/2018/09/final-classes-by-default-why/>`_ and `When to declare classes final <http://ocramius.github.io/blog/when-to-declare-classes-final/>`_.


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/FinalByOcramius                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.4                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Features     | final                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


