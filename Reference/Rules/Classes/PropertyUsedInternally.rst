.. _classes-propertyusedinternally:

.. _internally-used-properties:

Internally Used Properties
++++++++++++++++++++++++++

  Properties that are used internally.

.. code-block:: php
   
   <?php
   
   class x {
       public $internallyUsedProperty = 1;
       public $externallyUsedProperty = 1;
       public $alsoExternallyUsedProperty = 1;
       
       function foo() {
           $this->internallyUsedProperty = 2;
       }
   }
   
   class y extends x {
       function bar() {
           $this->externallyUsedProperty = 3;
       }
   }
   
   $X = new x();
   $X->alsoExternallyUsedProperty = 3;
   
   ?>
Connex PHP features
-------------------

  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/PropertyUsedInternally                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


