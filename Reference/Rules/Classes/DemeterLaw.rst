.. _classes-demeterlaw:

.. _law-of-demeter:

Law of Demeter
++++++++++++++

  The law of Demeter specifies a number of constraints to apply to methodcalls from within an method, so as to keep dependencies to a minimum. 


.. code-block:: php
   
   <?php
   
   class x {
       function foo($arg) {
           $this->foo();    // calling oneself is OK
           $this->x->bar(); // calling one's property is OK
           $arg->bar2();    // calling arg's methods is OK
   
           $local = new y();
           $z = $y->bar3();      // calling a local variable is OK
   
           $z->bar4();      // calling a method on a previous result is wrong
       }
   }
   
   ?>

See also `Do your objects talk to strangers? <https://www.brandonsavage.net/do-your-objects-talk-to-strangers/>`_ and `Law of Demeter <https://en.wikipedia.org/wiki/Law_of_Demeter>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/DemeterLaw                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.7                                                                                                                   |
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


