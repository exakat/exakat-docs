.. _functions-hasfluentinterface:

.. _method-has-fluent-interface:

Method Has Fluent Interface
+++++++++++++++++++++++++++

  Mark a method when it only returns `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_.

Fluent interfaces allows for chaining methods calls. This implies that `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ is always returned, so that the next method call is done on the same object.


.. code-block:: php
   
   <?php
   
   $object = new foo();
   $object->this()
          ->is()
          ->a()
          ->fluent()
          ->interface();
          
   class foo {
       function this() {
           // doSomething
           return $this;
       }
   
       function is() {
           // doSomethingElse
           return $this;
       }
       
       /// Etc. for a(), fluent(), interface()...
   }
   
   ?>

See also `Fluent Interfaces in PHP <http://mikenaberezny.com/2005/12/20/fluent-interfaces-in-php/>`_ and `Fluent Interfaces are Evil <https://ocramius.github.io/blog/fluent-interfaces-are-evil/>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/HasFluentInterface                                                                                            |
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
| Features     | class                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


