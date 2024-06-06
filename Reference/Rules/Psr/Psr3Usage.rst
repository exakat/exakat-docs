.. _psr-psr3usage:

.. _psr-3-usage:

PSR-3 Usage
+++++++++++

  PSR-3 describes a common interface for logging libraries.

It is supported by an set of interfaces, that one may use in the code.

.. code-block:: php
   
   <?php
   
   namespace MyNamespace;
   
   // MyLog implements the PSR-3 LoggerInterface.
   // MyLog is more of a black hole than a real Log.
   namespace ;
   
   class MyLog implements \Psr\Log\LoggerInterface {
       public function emergency($message, array $context = array()) {}
       public function alert($message, array $context = array()) {}
       public function critical($message, array $context = array()) {}
       public function error($message, array $context = array()) {}
       public function warning($message, array $context = array()) {}
       public function notice($message, array $context = array()) {}
       public function info($message, array $context = array()) {}
       public function debug($message, array $context = array()) {}
       public function log($level, $message, array $context = array()) {}
   }
   
   ?>

See also `PSR-3 : Logger Interface <http://www.php-fig.org/psr/psr-3/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Psr/Psr3Usage                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.6                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | psr                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


