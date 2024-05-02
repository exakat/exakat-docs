.. _classes-classusage:

.. _class-usage:

Class Usage
+++++++++++

  List of classes in use in the code source.

.. code-block:: php
   
   <?php
   
   // Class may be used in a use expression
   use MyClass as MyAliasedClass;
   
   // class may be aliased with class_alias
   class_alias('MyOtherAliasedClass', 'MyClass');
   
   // Class may be instanciated
   $o = new MyClass();
   
   // Class may be used with instanceof
   var_dump($o instanceof \MyClass);
   
   // Class may be used in static calls
   MyClass::aConstant;
   echo MyClass::$aProperty;
   echo MyClass::aMethod( $o );
   
   // Class may be extended
   class MyOtherClass {
   
   }
   
   class MyClass extends MyOtherClass {
       const aConstant = 1;
       
       public static $aProperty = 2;
       
       // also used as a typehint
       public static function aMethod(MyClass $object) {
           return __METHOD__;
       }
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ClassUsage                                                                                                      |
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


