.. _php-nativeclasstypecompatibility:

.. _php-native-class-type-compatibility:

PHP Native Class Type Compatibility
+++++++++++++++++++++++++++++++++++

  PHP enforces the method compatibility with native classes and interfaces. 

This means that classes that extends native PHP classes or interfaces must declare compatible types. They can't omit typing, like it was the case until PHP 8.0.


.. code-block:: php
   
   <?php
   
   class a extends RecursiveFilterIterator { 
   
       // fully declared method
       function hasChildren(): bool {
           return true;
       }
   
       // key() returns mixed. Omitting the type used to be quiet
       function key() {}
       
       //    #[\ReturnTypeWillChange] is taken into account 
   
   }
   ?>


This is needed for compatibility with PHP 8.0. This is probably good for older versions too, although it is not reported.

The `attribute <https://www.php.net/attribute>`_ ``ReturnTypeWillChange`` is taken into account by this rule. Note that it is not detected when auditing with PHP < 8.0, so it won't have effect until this version. The `attribute <https://www.php.net/attribute>`_ was declared in PHP 8.1, though it is also taken into account when auditing with PHP 8.0.

See also method-compatibility.


Suggestions
___________

* Make sure the methods are compatible or identical to the parent's method signature.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/NativeClassTypeCompatibility                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | returntypewillchange, type-covariance, type-contravariance                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


