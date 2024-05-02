.. _structures-uselessnullcoalesce:

.. _useless-null-coalesce:

Useless Null Coalesce
+++++++++++++++++++++

  When the type system ensure the condition is never null, the operator becomes useless. 

This is particularly true for properties (`static <https://www.php.net/manual/en/language.oop5.static.php>`_ or not) and returntype of methods and functions. And, to a lesser extend, to variables and parameters.

.. code-block:: php
   
   <?php
   
   function foo(A $a, ?B $b) {
       // $a is never null, so this is OK
       $a ?? 'a';
       
       // $b might be null, so this is OK
       $b ?? 'b';
   }
   
   ?>

See also `Null coalescing operator <https://www.php.net/manual/en/migration70.new-features.php#migration70.new-features.null-coalesce-op>`_.


Suggestions
___________

* Remove the ?? operator
* Switch to a ?: operator
* Updated the properties to accept NULL as a possible type




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UselessNullCoalesce                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | coalesce                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


