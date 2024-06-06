.. _classes-couldbeprivatemethod:

.. _method-could-be-private-method:

Method Could Be Private Method
++++++++++++++++++++++++++++++

  The following methods are never used outside their class of definition. Given the analyzed code, they could be set as private. 
Note that dynamic properties (such as $x->$y) are not taken into account.

.. code-block:: php
   
   <?php
   
   class foo {
       public function couldBePrivate() {}
       public function cantdBePrivate() {}
       
       function bar() {
           // couldBePrivate is used internally. 
           $this->couldBePrivate();
       }
   }
   
   class foo2 extends foo {
       function bar2() {
           // cantdBePrivate is used in a child class. 
           $this->cantdBePrivate();
       }
   }
   
   //couldBePrivate() is not used outside 
   $foo = new foo();
   
   //cantdBePrivate is used outside the class
   $foo->cantdBePrivate();
   
   ?>

Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBePrivateMethod                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.11                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Features     | private, method                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


