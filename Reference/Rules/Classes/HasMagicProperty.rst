.. _classes-hasmagicproperty:

.. _has-magic-method:

Has Magic Method
++++++++++++++++

  The class has defined one of the magic methods.

The magic methods are  : `__call() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__callStatic() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__get() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__set() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__isset() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__unset() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__sleep() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__wakeup() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__toString() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__invoke() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__set_state() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__clone() <https://www.php.net/manual/en/language.oop5.magic.php>`_ and `__debugInfo() <https://www.php.net/manual/en/language.oop5.magic.php>`_.

`__construct() <https://www.php.net/manual/en/language.oop5.decon.php>`_ and `__destruct() <https://www.php.net/manual/en/language.oop5.decon.php>`_ are omitted here. 


.. code-block:: php
   
   <?php
   
   class WithMagic {
       // some more methods, const or properties
       
       public function __get() {
           // doSomething();
       }
   }
   
   ?>

See also `Property overloading <https://www.php.net/manual/en/language.oop5.overloading.php#language.oop5.overloading.members>`_..


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/HasMagicProperty                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | magic-method                                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


