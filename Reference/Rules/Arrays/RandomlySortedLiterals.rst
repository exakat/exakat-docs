.. _arrays-randomlysortedliterals:

.. _randomly-sorted-arrays:

Randomly Sorted Arrays
++++++++++++++++++++++

  Those literal arrays are written in several places, but their items are in various orders. 

This may reduce the reading and proofing of the arrays, and induce confusion. The random order may also be a residue of development : both arrays started with different values, but they grew overtime to handle the same items. The way they were written lead to the current order.

Unless order is important, it is recommended to always use the same order when defining literal arrays. This makes it easier to match different part of the code by recognizing one of its literal.

.. code-block:: php
   
   <?php
   
   // an array
   $set = [1,3,5,9,10];
   
   function foo() {
       // an array, with the same values but different order, in a different context
       $list = [1,3,5,10,9,];
   }
   
   // an array, with the same order than the initial one
   $inits = [1,3,5,9,10];
   
   ?>

+---------+---------+---------+-----------------------------------+
| Name    | Default | Type    | Description                       |
+---------+---------+---------+-----------------------------------+
| maxSize | 5       | integer | Maximal size of arrays to survey. |
+---------+---------+---------+-----------------------------------+



Suggestions
___________

* Match the sorting order of the arrays. Choose any of them.
* Configure a constant and use it as a replacement for those arrays.
* Leave the arrays intact : the order may be important.
* For hash arrays, consider turning the array in a class.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/RandomlySortedLiterals                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Suggestions <ruleset-Suggestions>`                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.2                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | array                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-contao-arrays-randomlysortedliterals`, :ref:`case-vanilla-arrays-randomlysortedliterals`                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


