.. _classes-hasfluentinterface:

.. _class-has-fluent-interface:

Class Has Fluent Interface
++++++++++++++++++++++++++

  Mark a class as such when it contains at least one fluent method. A fluent method is a method that returns `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_, for chaining.

.. code-block:: php
   
   <?php
   
   class foo {
       private $count = 0;
   
       function a() {
           ++$this->count;
           return $this;
       }
   
       function b() {
           $this->count += 2;
           return $this;
       }
   
       function c() {
           return $this->count;
       }
   }
   
   $bar = new foo();
   print $bar->a()
             ->b()
             ->c();
   
   // display 3 (1 + 2).
   
   ?>

See also `Fluent interface are evil <https://ocramius.github.io/blog/fluent-interfaces-are-evil/>`_, `The basics of Fluent interfaces in PHP <https://tournasdimitrios1.wordpress.com/2011/04/11/the-basics-of-fluent-interfaces-in-php/>`_ and `FluentInterface <https://martinfowler.com/bliki/FluentInterface.html>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/HasFluentInterface                                                                                              |
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
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | fluent-interface                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


