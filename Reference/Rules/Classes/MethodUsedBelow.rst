.. _classes-methodusedbelow:

.. _method-used-below:

Method Used Below
+++++++++++++++++

  Mark methods that are used in children classes.


.. code-block:: php
   
   <?php
   
   class foo {
       // This method is used in children
       protected function protectedMethod() {}
       
       // This method is not used in children
       protected function localProtectedMethod() {}
   
       private function foobar() {
           // protectedMethod is used here, but defined in parent
           $this->localProtectedMethod();
       }
   }
   
   class foofoo extends foo {
       private function bar() {
           // protectedMethod is used here, but defined in parent
           $this->protectedMethod();
       }
   }
   
   ?>


This doesn't mark the current class, nor the (grand-)`parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ ones.

See also inheritance.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MethodUsedBelow                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.11                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | method                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


