.. _structures-uselesstrailingcomma:

.. _useless-trailing-comma:

Useless Trailing Comma
++++++++++++++++++++++

  Trailing comma is the last comma in a call or function definition. It is left with an empty slot aftewards, so as to reduce the diff when adding or removing an element. 

Trailing commas appear in array definition, method calls, method definitions, including use expression for closures and use call. 

Trailing comma with only one element are reported as useless. Then, for multiple elements, the elements should be on separate lines.

This is a coding convention.


.. code-block:: php
   
   <?php
   
   $good = array(1,
   			  2,
   			  3,
   			  4,
   			  );
   
   // The trailing comma is just useless.
   $bad = array( 1, 2, 3, 4, );
   
   ?>

Suggestions
___________

* Remove the trailing comma
* Put the trailing comma on a new line




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UselessTrailingComma                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Coding conventions <ruleset-Coding-conventions>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | trailing comma                                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


