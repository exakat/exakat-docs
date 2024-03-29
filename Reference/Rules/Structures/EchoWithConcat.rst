.. _structures-echowithconcat:

.. _echo-with-concat:

Echo With Concat
++++++++++++++++

  Optimize your ``echo``'s by avoiding concatenating at ``echo`` time, but serving all argument separated. This will save PHP a memory copy.

If values, literals and variables, are small enough, this won't have visible impact. Otherwise, this is less work and less memory waste.


.. code-block:: php
   
   <?php
     echo $a, ' b ', $c;
   ?>


instead of


.. code-block:: php
   
   <?php
     echo  $a . ' b ' . $c;
     echo $a b $c;
   ?>


It is a micro-optimisation.

Suggestions
___________

* Turn the concatenation into a list of argument, by replacing the dots by commas.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/EchoWithConcat                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Performances <ruleset-Performances>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | echo                                                                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-unnecessary-string-concatenation <https://github.com/dseguy/clearPHP/tree/master/rules/no-unnecessary-string-concatenation.md>`__            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phpdocumentor-structures-echowithconcat`, :ref:`case-teampass-structures-echowithconcat`                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------+


