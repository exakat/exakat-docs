.. _structures-functionpresubscripting:

.. _function-subscripting,-old-style:

Function Subscripting, Old Style
++++++++++++++++++++++++++++++++

  It is possible use function results as an array, and read directly its element. This was added in PHP 5.4.

.. code-block:: php
   
   <?php
   
   function foo() {
       return array(1 => 'a', 'b', 'c');
   }
   
   echo foo()[1]; // displays 'a';
   
   // Function subscripting, the old way
   function foo() {
       return array(1 => 'a', 'b', 'c');
   }
   
   $x = foo();
   echo $x[1]; // displays 'a';
   
   ?>
Connex PHP features
-------------------

  + `function-subscripting <https://php-dictionary.readthedocs.io/en/latest/dictionary/function-subscripting.ini.html>`_


Suggestions
___________

* Skip the local variable and directly use the return value from the function




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/FunctionPreSubscripting                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.4 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-openconf-structures-functionpresubscripting`                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


