.. _classes-magicmethod:

.. _magic-methods:

Magic Methods
+++++++++++++

  List of PHP magic methods being used. The magic methods are 

`__call() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__callStatic() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__get() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__set() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__isset() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__unset() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__sleep() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__wakeup() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__toString() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__invoke() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__set_state() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__clone() <https://www.php.net/manual/en/language.oop5.magic.php>`_ and `__debugInfo() <https://www.php.net/manual/en/language.oop5.magic.php>`_.

``__construct`` and ``__destruct`` are omitted here, as they are routinely used to create and destroy objects.


.. code-block:: php
   
   <?php
   
   class foo{
       // PHP Magic method, called when cloning an object.
       function __clone() {}
   }
   ?>

Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MagicMethod                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
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


