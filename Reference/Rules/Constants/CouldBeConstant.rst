.. _constants-couldbeconstant:

.. _could-be-constant:

Could Be Constant
+++++++++++++++++

  Literals may be replaced by an existing constant. 

Constants makes the code easier to read, as they may bear a meaningful name. They also hide implementation values, with a readable name, such as ``const READABLE= true;``. Later, upgrading constant values is easier than scouring the code with a new literal. 

Not all literal can be replaced by a constant values : sometimes, literal may have the same literal value, but different meanings. Check with your application semantics before changing any literal with a constant.


.. code-block:: php
   
   <?php
   
   const A = 'abc';
   define('B', 'ab');
   
   class foo {
       const X = 'abcd';
   }
   
   // Could be replaced by B;
   $a = 'ab'; 
   
   // Could be replaced by A;
   $a = 'abc'; 
   
   // Could be replaced by foo::X;
   $a = 'abcd'; 
   
   ?>


This analysis currently doesn't support arrays. 

This analysis also skips very common values, such as boolean, ``0`` and ``1``. This prevents too many false positive.

Suggestions
___________

* Turn the literal into an existing constant




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/CouldBeConstant                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Semantics <ruleset-Semantics>`                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | constant                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


