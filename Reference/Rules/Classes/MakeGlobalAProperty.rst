.. _classes-makeglobalaproperty:

.. _make-global-a-property:

Make Global A Property
++++++++++++++++++++++

  Calling global (or $GLOBALS) in methods is slower and less testable than setting the global to a property, and using this property.

Using properties is slightly faster than calling global or $GLOBALS, though the gain is not important. 

Setting the property in the constructor (or in a factory), makes the class easier to test, as there is now a single point of configuration.

.. code-block:: php
   
   <?php 
   
   // Wrong way
   class fooBad {
       function x() {
           global $a;
           $a->do();
           // Or $GLOBALS['a']->do();
       }
   }
   
   class fooGood {
       private $bar = null;
       
       function __construct() {
           global $bar; 
           $this->bar = $bar;
           // Even better, do this via arguments
       }
       
       function x() {
           $this->a->do();
       }
   }
   
   ?>

Suggestions
___________

* Avoid using global variables, and use properties instead
* Remove the usage of these global variables




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MakeGlobalAProperty                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | class, global-variable                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


