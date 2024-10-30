.. _classes-couldbeprotectedproperty:

.. _could-be-protected-property:

Could Be Protected Property
+++++++++++++++++++++++++++

  Those properties are declared public, but are never used publicly. They may be made protected. 

This property may even be made private.

.. code-block:: php
   
   <?php
   
   class foo {
       // Public, and used publicly
       public $publicProperty;
       // Public, but never used outside the class or its children
       public $protectedProperty;
       
       function bar() {
           $this->protectedProperty = 1;
       }
   }
   
   $foo = new Foo();
   $foo->publicProperty = 3;
   
   ?>
Connex PHP features
-------------------

  + `visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/visibility.ini.html>`_


Suggestions
___________

* Use protected visibility with these properties.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBeProtectedProperty                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.7                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


