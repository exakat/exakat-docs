.. _classes-unreachableconstant:

.. _unreachable-class-constant:

Unreachable Class Constant
++++++++++++++++++++++++++

  Class constants may be unreachable due to visibility configuration. 

Since PHP 7.1, class constants support visibility. Their usage may be restricted to the current class, or ``private``, to classes that extends or are extended by the current class, or ``protected``. They may also be ``public``, just like it was before.

.. code-block:: php
   
   <?php
   
   class Foo{
       private const PRIVATE = 1;
               const PUBLIC = 3;
   }
   
   // PHP 7.1- and older
   echo Foo::PUBLIC;
   
   // This is not accessible
   echo Foo::PRIVATE;
   
   ?>

See also `Class Constant <https://www.php.net/manual/en/language.oop5.constants.php>`_ and `PHP RFC: Support Class Constant Visibility <https://wiki.php.net/rfc/class_const_visibility>`_.


Suggestions
___________

* Make the class constant protected, when the call to the constant is inside a related class.
* Create another constant, that may be accessible
* Make the class constant public




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UnreachableConstant                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Class Review <ruleset-Class-Review>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | class                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


