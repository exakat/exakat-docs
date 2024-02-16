.. _structures-missingnew:

.. _maybe-missing-new:

Maybe Missing New
+++++++++++++++++

  This functioncall looks like a class instantiation that is missing the new keyword.

Any function definition was found for that function, but a class with that name was. New is probably missing.

.. code-block:: php
   
   <?php
   
   // Functioncall
   $a = foo();
   
   // Class definition
   class foo {}
   // Function definition
   function foo {}
   
   
   // Functioncall
   $a = BAR;
   
   // Function definition
   class bar {}
   // Constant definition
   const BAR = 1;
   
   
   ?>

Suggestions
___________

* Add the new
* Rename the class to distinguish it from the function
* Rename the function to distinguish it from the class




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MissingNew                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | new                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


