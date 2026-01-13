.. _functions-couldtypehint:

.. _could-typehint:

Could Typehint
++++++++++++++

  Arguments that are tested with `instanceof <https://www.php.net/manual/en/language.operators.type.php>`_, `is_array() <https://www.php.net/is_array>`_, `is_string() <https://www.php.net/is_string>`_, etc. could be modernized with a typehint.

.. code-block:: php
   
   <?php
   
   function foo($a, $b) {
       // $a is tested for B with instanceof. 
       if (!$a instanceof B) {
           return;
       }
       
       // More code
   }
   
   function foo(B $a, $b) {
       // May omit the initial test
       
       // More code
   }
   
   ?>
Connex PHP features
-------------------

  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_


Suggestions
___________

* Add the typehint, remove the test on the type




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/CouldTypehint                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.5                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


