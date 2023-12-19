.. _patterns-gettersetter:

.. _getter-and-setter:

Getter And Setter
+++++++++++++++++

  A getter is a method whose purpose is to read the internal value of a class; a setter is a method whose purpose is to write a value inside a class. 

Exakat marks simple setters and getters : their content only writes (resp. reads) on property at a time. More refined getters/setters might appear in the future, when formatting and filter is detected and omitted. 


.. code-block:: php
   
   <?php
   
   class x {
       private $p = 1;
       
       // getter
       function getP() {
           return $this->p;
       }
   
       // setter
       function setP($a) {
           $this->p = $a;
       }
   }
   
   ?>

See also `PHP: Getters and Setters <https://thisinterestsme.com/php-getters-and-setters/>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Patterns/GetterSetter                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | getter, setter                                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


