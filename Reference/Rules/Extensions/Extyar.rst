.. _extensions-extyar:

.. _extensions-yar:

Extensions yar
++++++++++++++

  yar : Yet Another RPC framework. 


.. code-block:: php
   
   <?php
   
   /* assume this page can be accessed by http://example.com/operator.php */
   
   class Operator {
   
       /**
        * Add two operands
        * @param interge 
        * @return interge
        */
       public function add($a, $b) {
           return $this->_add($a, $b);
       }
   
       /**
        * Sub 
        */
       public function sub($a, $b) {
           return $a - $b;
       }
   
       /**
        * Mul
        */
       public function mul($a, $b) {
           return $a * $b;
       }
   
       /**
        * Protected methods will not be exposed
        * @param interge 
        * @return interge
        */
       protected function _add($a, $b) {
           return $a + $b;
       }
   }
   
   $server = new Yar_Server(new Operator());
   $server->handle();
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extyar                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | rpc                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


