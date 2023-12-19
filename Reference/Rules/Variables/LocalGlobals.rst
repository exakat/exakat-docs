.. _variables-localglobals:

.. _local-globals:

Local Globals
+++++++++++++

  A global variable is used locally in a method. 

Either the global keyword has been forgotten, or the local variable should be renamed in a less ambiguous manner.

Having both a global and a local variable with the same name is legit. PHP keeps the contexts separated, and it processes them independently.

However, in the mind of the coder, it is easy to mistake the local variable $x and the global variable $x. May they be given different meaning, and this is an `error <https://www.php.net/error>`_-prone situation. 

It is recommended to keep the global variables's name distinct from the local variables. 


.. code-block:: php
   
   <?php
   
   // This is actualy a global variable
   $variable = 1;
   $globalVariable = 2;
   
   function foo() {
       global $globalVariable2;
       
       $variable = 4;
       $localVariable = 3;
       
       // This always displays 423, instead of 123
       echo $variable .' ' . $globalVariable . ' ' . $localVariable;
   }
   
   ?>

Suggestions
___________

* Add the global keyword for that variable
* Change the name of the variable for another one, which is not a global variable




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/LocalGlobals                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | global                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


