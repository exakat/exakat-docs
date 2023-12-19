.. _functions-modifytypedparameter:

.. _modified-typed-parameter:

Modified Typed Parameter
++++++++++++++++++++++++

  Reports modified parameters, which have a non-scalar typehint. Such variables should not be changed within the body of the method. Unlike typed properties, which always hold the expected type, typed parameters are only guaranteed type at the beginning of the method block. 


.. code-block:: php
   
   <?php
   
   class x {
   
       function foo(Y $y) {
           // $y is type Y
   
           // A cast version of $y is stored into $yAsString. $y is untouched.
           $yAsString = (string) $y;
   
           // $y is of type 'int', now.
           $y = 1;
   
           // Some more code
   
           // display the string version.
           echo $yAsString; 
           // so, Y $y is now raising an error
           echo $y->name; 
       }
   }
   
   ?>


This problem doesn't apply to scalar types : by default, PHP pass scalar parameters by value, not by reference. Class types are always passed by reference.

This problem is similar to :ref:`don't-unset-properties`  : the `static <https://www.php.net/manual/en/language.oop5.static.php>`_ specification of the property may be unset, leading to confusing 'undefined property', while the class hold the property definition.

Suggestions
___________

* Use different variable names when converting a parameter to a different type.
* Only use methods and properties calls on a typed parameter.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/ModifyTypedParameter                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | typehint, parameter                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


