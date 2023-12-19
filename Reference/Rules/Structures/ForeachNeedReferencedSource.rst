.. _structures-foreachneedreferencedsource:

.. _foreach-needs-reference-array:

Foreach Needs Reference Array
+++++++++++++++++++++++++++++

  When using foreach with a reference as value, the source must be a referenced array, which is a variable (or array or property or `static <https://www.php.net/manual/en/language.oop5.static.php>`_ property). 
When the array is the `result <https://www.php.net/result>`_ of an expression, the array is not kept in memory after the foreach loop, and any change made with & are lost.

This will do nothing


.. code-block:: php
   
   <?php
       foreach(array(1,2,3) as &$value) {
           $value *= 2;
       }
   ?>


This will have an actual effect


.. code-block:: php
   
   <?php
       $array = array(1,2,3);
       foreach($array as &$value) {
           $value *= 2;
       }
   ?>

Suggestions
___________

* Use a referenced array when applying modifications inside a foreach loop




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ForeachNeedReferencedSource                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
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
| Features     | foreach, reference                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


