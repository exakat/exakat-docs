.. _interfaces-alreadyparentsinterface:

.. _already-parents-interface:

Already Parents Interface
+++++++++++++++++++++++++

  The same interface is implemented by a class and one of its children. 

That way, the child doesn't need to implement the interface, nor define its methods to be an instance of the interface. 


.. code-block:: php
   
   <?php
   
   interface i { 
       function i();
   }
   
   class A implements i {
       function i() {
           return __METHOD__;
       }
   }
   
   // This implements is useless. 
   class AB extends A implements i {
       // No definition for function i()
   }
   
   // Implements i is understated
   class AB extends A {
       // redefinition of the i method
       function i() {
           return __METHOD__.' ';
       }
   }
   
   $x = new AB;
   var_dump($x instanceof i);
   // true
   
   $x = new AC;
   var_dump($x instanceof i);
   // true
   
   ?>


This analysis may report classes which do not explicitly implements any interfaces : the issue is then coming from the parents.

Suggestions
___________

* Keep the implements call in the class that do implements the methods. Remove it from the children classes.




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Interfaces/AlreadyParentsInterface                                                                                                                                                               |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`IsExt <ruleset-IsExt>`, :ref:`IsPHP <ruleset-IsPHP>`, :ref:`IsStub <ruleset-IsStub>`, :ref:`Suggestions <ruleset-Suggestions>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                                                                            |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                                                                                              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                                                                            |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Instant (5 mins)                                                                                                                                                                                 |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                                        |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features         | implements, inheritance                                                                                                                                                                          |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Configurable by  | php_core, php_extensions, stubs                                                                                                                                                                  |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples         | :ref:`case-wordpress-interfaces-alreadyparentsinterface`, :ref:`case-thelia-interfaces-alreadyparentsinterface`                                                                                  |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                          |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


