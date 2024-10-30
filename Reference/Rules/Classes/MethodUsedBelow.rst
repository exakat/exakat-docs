.. _classes-methodusedbelow:

.. _method-used-below:

Method Used Below
+++++++++++++++++

  Mark methods that are used in children classes.
This doesn't mark the current class, nor the (grand-)`parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ ones.

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

See also inheritance.

Connex PHP features
-------------------

  + `method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MethodUsedBelow                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
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
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


