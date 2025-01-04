.. _php-versioncompareoperator:

.. _version\_compare-operator:

version_compare Operator
++++++++++++++++++++++++

.. meta::
	:description:
		version_compare Operator: version_compare()'s third argument is checked for value.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: version_compare Operator
	:twitter:description: version_compare Operator: version_compare()'s third argument is checked for value
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: version_compare Operator
	:og:type: article
	:og:description: version_compare()'s third argument is checked for value
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/version_compare Operator.html
	:og:locale: en
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
Related PHP errors 
-------------------

  + `version_compare(): Argument #3 ($operator) must be a valid comparison operator <https://php-errors.readthedocs.io/en/latest/messages/must-be-a-valid-comparison-operator.html>`_




Suggestions
___________

* Use a valid comparison operator




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/VersionCompareOperator                                                                                                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>`, :ref:`CompatibilityPHP82 <ruleset-CompatibilityPHP82>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.1                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


