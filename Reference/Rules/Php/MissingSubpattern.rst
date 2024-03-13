.. _php-missingsubpattern:

.. _possible-missing-subpattern:

Possible Missing Subpattern
+++++++++++++++++++++++++++

  When capturing subpatterns are the last ones in a regex, PHP doesn't fill their spot in the resulting array. This leads to a possible missing index in the `result <https://www.php.net/result>`_ array.
The same applies to `preg_replace() <https://www.php.net/preg_replace>`_ : the pattern may match the string, but no value is available is the corresponding sub-pattern.

In PHP 7.4, a new option was added : ``PREG_UNMATCHED_AS_NULL``, which always provides a value for the subpatterns.

.. code-block:: php
   
   <?php
   
   // displays a partial array, from 0 to 1
   preg_match('/(a)(b)?/', 'adc', $r);
   print_r($r);
   /*
   Array
   (
       [0] => a
       [1] => a
   )
   */
   
   // displays a full array, from 0 to 2
   preg_match('/(a)(b)?/', 'abc', $r);
   print_r($r);
   
   /*
   Array
   (
       [0] => ab
       [1] => a
       [2] => b
   )
   */
   
   // double 'b' when it is found
   print preg_replace(',^a(b)?,', './$1$1', 'abc'); // prints ./abbc
   print preg_replace(',^a(b)?,', './$1$1', 'adc'); // prints ./dc
   
   ?>

See also `Bug #73948 Preg_match_all should return NULLs on trailing optional capture groups. <https://bugs.php.net/bug.php?id=73948>`_ and `Bug #50887 preg_match , last optional sub-patterns ignored when empty <https://bugs.php.net/bug.php?id=50887>`_.


Suggestions
___________

* Add an always capturing subpatterns after the last ?
* Move the ? inside the parenthesis, so the parenthesis is always on, but the content may be empty
* Add a test on the last index of the resulting array, to ensure it is available when needed
* Use the PREG_UNMATCHED_AS_NULL option (PHP 7.4+)




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/MissingSubpattern                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.1                                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | regex                                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phpmyadmin-php-missingsubpattern`, :ref:`case-spip-php-missingsubpattern`                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


