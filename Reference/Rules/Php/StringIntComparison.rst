.. _php-stringintcomparison:

.. _string-int-comparison:

String Int Comparison
+++++++++++++++++++++

  While PHP allows direct comparison of integer and strings, with some type conversion, the rules of conversion changed in PHP 8.0. This lead to a change in behavior for comparison.

In particular, strings that are equal to 0, or empty strings, have changed.

This doesn't affect identity comparison, since the type is initially checked.

.. code-block:: php
   
   <?php
                           PHP 7   PHP 8
   var_dump(0 == "0");  	true 	true
   var_dump(0 == "0.0"); 	true 	true
   var_dump(0 == "foo");   false   false
   
   var_dump(0 > '');       false   true
   var_dump(0 < '');       false   false
   var_dump(0 >= '');      true    true
   var_dump(0 <= '');      true    false
   
   ?>

See also `String to Number Comparison <https://www.php.net/manual/en/migration80.incompatible.php#migration80.incompatible.core.string-number-comparision>`_.

Connex PHP features
-------------------

  + `comparison <https://php-dictionary.readthedocs.io/en/latest/dictionary/comparison.ini.html>`_


Suggestions
___________

* Force a conversion to integer before the comparison to make sure of the behavior.




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/StringIntComparison                                                                                                              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 2.3.9                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 8.0 and more recent                                                                                                         |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                      |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.0 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/.html>`__                                           |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Medium                                                                                                                               |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+


