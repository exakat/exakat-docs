.. _classes-couldbeclassconstant:

.. _could-be-class-constant:

Could Be Class Constant
+++++++++++++++++++++++

  When a property is defined and read, but never modified, it could be turned into a constant. 


.. code-block:: php
   
   <?php
   
   class foo {
       // $this->bar is never modified. 
       private $bar = 1;
       
       // $this->foofoo is modified, at least once
       private $foofoo = 2;
       
       function method($a) {
           $this->foofoo = $this->bar + $a + $this->foofoo;
           
           return $this->foofoo;
       }
       
   }
   
   ?>


Starting with PHP 5.6, `array() <https://www.php.net/array>`_ may be defined as constants.

See also Class Constants `<https://www.php.net/manual/en/language.oop5.constants.php>`_.


Suggestions
___________

* Turn the property into a class constant




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBeClassConstant                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Class Review <ruleset-Class-Review>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | class-constant, visibility                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


