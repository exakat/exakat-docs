.. _functions-withoutreturn:

.. _methods-without-return:

Methods Without Return
++++++++++++++++++++++

  List of all the functions, closures, methods that have no explicit return. 

Functions with the ``void`` or ``never`` return types, are omitted.

.. code-block:: php
   
   <?php
   
   // With return null : Explicitly not returning
   function withExplicitReturn($a = 1) {
       $a++;
       return null;
   }
   
   // Without indication
   function withoutExplicitReturn($a = 1) {
       $a++;
   }
   
   // With return type void : Explicitly not returning
   function withExplicitReturnType($a = 1) : void {
       $a++;
   }
   
   ?>

See also `return <https://www.php.net/manual/en/function.return.php>`_.


Suggestions
___________

* Add the returntype 'void' to make this explicit behavior




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/WithoutReturn                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | return, never                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


