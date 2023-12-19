.. _extensions-extweakref:

.. _ext-weakref:

ext/weakref
+++++++++++

  Weak References for PHP.

Weak references provide a non-intrusive gateway to ephemeral objects. Unlike normal (strong) references, weak references do not prevent the garbage collector from freeing that object. For this reason, an object may be destroyed even though a weak reference to that object still exists. In such conditions, the weak reference seamlessly becomes invalid.


.. code-block:: php
   
   <?php
   class MyClass {
       public function __destruct() {
           echo "Destroying object!\n";
       }
   }
   
   $o1 = new MyClass;
   
   $r1 = new WeakRef($o1);
   
   if ($r1->valid()) {
       echo "Object still exists!\n";
       var_dump($r1->get());
   } else {
       echo "Object is dead!\n";
   }
   
   unset($o1);
   
   if ($r1->valid()) {
       echo "Object still exists!\n";
       var_dump($r1->get());
   } else {
       echo "Object is dead!\n";
   }
   ?>

See also `Weak references <https://www.php.net/manual/en/book.weakref.php>`_ and `PECL extension that implements weak references and weak maps in PHP <https://github.com/colder/php-weakref>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extweakref                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.5                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


