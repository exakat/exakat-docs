.. _classes-mismatchproperties:

.. _mismatch-properties-typehints:

Mismatch Properties Typehints
+++++++++++++++++++++++++++++

  Properties must match within the same family.

When a property is declared both in a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class, and a child class, they must have the same type. The same type includes a possible null value.

This doesn't apply to private properties, which are only visible locally.


.. code-block:: php
   
   <?php
   
   // property $p is declared as an object of type a
   class x { 
       protected A $p; 
   }
   
   // property $p is declared again, this time without a type
   class a extends x { 
       protected $p; 
   }
   ?>


This code will lint, but not execute.

Suggestions
___________

* Remove some of the property declarations, and only keep it in the highest ranking parent
* Match the typehints of the property declarations
* Make the properties private
* Remove the child class (or the parent class)




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MismatchProperties                                                                                                                               |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.4                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | property                                                                                                                                                 |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+


