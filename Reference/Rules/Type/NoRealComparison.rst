.. _type-norealcomparison:

.. _no-real-comparison:

No Real Comparison
++++++++++++++++++

  Avoid comparing decimal numbers with ==, ===, !==, !=. Real numbers have an `error <https://www.php.net/error>`_ margin which is random, and makes it very difficult to match even if the compared value is a literal. 

PHP uses an internal representation in base 2 : any number difficult to represent with this base (like 0.1 or 0.7) will have a margin of `error <https://www.php.net/error>`_.


.. code-block:: php
   
   <?php
   
   $a = 1/7;
   $b = 2.0;
   
   // 7 * $a is a real, not an integer
   var_dump( 7 * $a === 1);
   
   // rounding error leads to wrong comparison
   var_dump( (0.1 + 0.7) * 10 == 8);
   // although
   var_dump( (0.1 + 0.7) * 10);
   // displays 8
   
   // precision formula to use with reals. Adapt 0.0001 to your precision needs
   var_dump( abs(((0.1 + 0.7) * 10) - 8) < 0.0001); 
   
   ?>


Use precision formulas with `abs() <https://www.php.net/abs>`_ to approximate values with a given precision, or avoid reals altogether.

See also `Floating point numbers <https://www.php.net/manual/en/language.types.float.php#language.types.float>`_.


Suggestions
___________

* Cast the values to integer before comparing
* Compute the difference, and keep it below a threshold
* Use the ``gmp`` or the ``bcmath`` extension to handle high precision numbers
* Change the 'precision' directive of PHP : ``ini_set('precision', 30)`` to make number larger
* Multiply by a power of ten, before casting to integer for the comparison
* Use floor(), ceil() or round() to compare the numbers, with a specific precision




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/NoRealComparison                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Top10 <ruleset-Top10>`                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | real                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-real-comparison <https://github.com/dseguy/clearPHP/tree/master/rules/no-real-comparison.md>`__                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-magento-type-norealcomparison`, :ref:`case-spip-type-norealcomparison`                                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


