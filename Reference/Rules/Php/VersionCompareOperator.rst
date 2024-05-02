.. _php-versioncompareoperator:

.. _version\_compare-operator:

version_compare Operator
++++++++++++++++++++++++

  `version_compare() <https://www.php.net/version_compare>`_'s third argument is checked for value. The third argument specifies the operator, which may be only one of the following : `<`, `lt`, `<=`, `le`, `>`, `gt`, `>=`, `ge`, `==`, `=`, `eq`, `!=`, `<>`, `ne`. The operator is case sensitive.

Until PHP 8.1, it was silently reverted to the default value. It is a deprecated warning in PHP 8.1 and will be finalized in PHP 9.0. It is recommended to fix this parameter in any PHP version.

.. code-block:: php
   
   <?php
   
   // return true
   var_dump(version_compare('2.0', '2.1', '<'));
   
   // returns false
   var_dump(version_compare('2.0', '2.1', '>'));
   
   // returns NULL and might be interpreted as false
   var_dump(version_compare('2.0', '2.1', 'as'));
   
   ?>

Suggestions
___________

* Use a valid comparison operator




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/VersionCompareOperator                                                                                                                                                 |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>`, :ref:`CompatibilityPHP82 <ruleset-CompatibilityPHP82>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.1                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                                                                               |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


