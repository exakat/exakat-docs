.. _structures-uselessshortternary:

.. _useless-short-ternary:

Useless Short Ternary
+++++++++++++++++++++

  The short ternary operates on empty or null values. When the type of the condition is not false, boolean or null, the operator is useless.

.. code-block:: php
   
   <?php
   
   function foo() : A { return new A; }
   
   // This is useless
   $b = foo() ? 1;
   
   ?>
Connex PHP features
-------------------

  + `short-ternary <https://php-dictionary.readthedocs.io/en/latest/dictionary/short-ternary.ini.html>`_


Suggestions
___________

* Remove the ternary operator
* Refactor the types to allow for empty values




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UselessShortTernary                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


