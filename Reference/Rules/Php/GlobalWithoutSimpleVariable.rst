.. _php-globalwithoutsimplevariable:

.. _simple-global-variable:

Simple Global Variable
++++++++++++++++++++++

  The global keyword should only be used with simple variables. Since PHP 7, it cannot be used with complex or dynamic structures.


.. code-block:: php
   
   <?php
   
   // Forbidden in PHP 7
   global $normalGlobal;
   
   // Forbidden in PHP 7
   global $$variable->global ;
   
   // Tolerated in PHP 7
   global ${$variable->global};
   
   ?>

See also `Changes to the handling of indirect variables, properties, and methods <https://www.php.net/manual/en/migration70.incompatible.php#migration70.incompatible.variable-handling.indirect>`_.


Suggestions
___________

* Add curly braces so the syntax is compatibles PHP 5 and PHP 7
* Remove this syntax, and access the variable through another way : argument, array, property.




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/GlobalWithoutSimpleVariable                                                                                                      |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 7.0 and older                                                                                                               |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Critical                                                                                                                             |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Slow (1 hour)                                                                                                                        |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.0                                                                                                                              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                            |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Features         | global                                                                                                                               |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+


