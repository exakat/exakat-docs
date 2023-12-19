.. _variables-inheritedstaticvariable:

.. _inherited-static-variable:

Inherited Static Variable
+++++++++++++++++++++++++

  `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ variables are distinct when used in an inherited `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method. In PHP 8.1, the `static <https://www.php.net/manual/en/language.oop5.static.php>`_ variable will also be inherited, and shared between the two methods, like a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ property.


.. code-block:: php
   
   <?php
   
   // Code extracted from the RFC
   class A {
       public static function counter() {
           static $i = 0;
           return ++$i;
       }
   }
   class B extends A {}
    
   var_dump(A::counter()); // int(1)
   var_dump(A::counter()); // int(2)
   var_dump(B::counter()); // int(1)
   var_dump(B::counter()); // int(2)
   
   ?>

See also `PHP RFC: Static variables in inherited methods <https://wiki.php.net/rfc/static_variable_inheritance>`_.


Suggestions
___________

* Define the method in the child class to enforce the distinct behavior
* Replace the static variable by a static property to make this PHP 8.1 ready




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Variables/InheritedStaticVariable                                                                                                    |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 2.2.2                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 8.0 and older                                                                                                               |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                      |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.1                                                                                                                              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Medium                                                                                                                               |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Features         | static-variable, inheritance                                                                                                         |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+


