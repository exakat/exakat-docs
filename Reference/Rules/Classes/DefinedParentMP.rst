.. _classes-definedparentmp:

.. _defined-parent-mp:

Defined Parent MP
+++++++++++++++++

  Check `static <https://www.php.net/manual/en/language.oop5.static.php>`_ calls with '`parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_'. 


.. code-block:: php
   
   <?php
   
   class foo {
       protected function parentDefined() {}
       protected function unusedParentMethod() {}
   
       // visibility is checked too
       protected function unusuableParentMethod() {}
   }
   
   class bar extends foo {
       
       private function someMethod() {
           // reported
           parent::parentDefined();
   
           // not reported, as method is unreachable in parent
           parent::unusuableParentMethod();
   
           // not reported, as method is undefined in parent
           parent::parentUndefined();
           
       }
   
       protected function parentDefined2() {}
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/DefinedParentMP                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


