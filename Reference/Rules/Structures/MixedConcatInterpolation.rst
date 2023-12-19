.. _structures-mixedconcatinterpolation:

.. _mixed-concat-and-interpolation:

Mixed Concat And Interpolation
++++++++++++++++++++++++++++++

  Mixed usage of concatenation and string interpolation is `error <https://www.php.net/error>`_ prone. It is harder to read, and leads to overlooking the concatenation or the interpolation.

Fixing this issue has no impact on the output. It makes code less `error <https://www.php.net/error>`_ prone.

There are some situations where using concatenation are compulsory : when using a constant, calling a function, running a complex expression or make use of the escape sequence. You may also consider pushing the storing of such expression in a local variable.



.. code-block:: php
   
   <?php
   
   // Concatenation string
   $a = $b . 'c' . $d;
   
   // Interpolation strings
   $a = "{$b}c{$d}";   // regular form
   $a = "{$b}c$d";     // irregular form
   
   // Mixed Concatenation and Interpolation string
   $a = "{$b}c" . $d;
   $a = $b . "c$d";
   $a = $b . "c{$d}";
   
   // Mixed Concatenation and Interpolation string with constant
   $a = "{$b}c" . CONSTANT;
   
   ?>

Suggestions
___________

* Only use one type of variable usage : either interpolation, or concatenation




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MixedConcatInterpolation                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Coding conventions <ruleset-Coding-conventions>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.5                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | interpolation, concat                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-suitecrm-structures-mixedconcatinterpolation`, :ref:`case-edusoho-structures-mixedconcatinterpolation`       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


