.. _php-noreferenceforternary:

.. _no-reference-for-ternary:

No Reference For Ternary
++++++++++++++++++++++++

  The ternary operator and the null coalescing operator are both expressions that only return values, and not a reference. 

This means that any provided reference will be turned into its value. While this is usually invisible, it will raise a warning when a reference is expected. This is the case with methods returning a reference. 

A PHP notice is generated when using a ternary operator or the null coalesce operator : ``Only variable references should be returned by reference``. The notice is also emitted when returning objects. 

This applies to methods, functions and closures.

.. code-block:: php
   
   <?php
   
   // This works
   function &foo($a, $b) { 
       if ($a === 1) {
           return $b; 
       } else {
           return $a; 
       }
   }
   
   // This raises a warning, as the operator returns a value
   function &foo($a, $b) { return $a === 1 ? $b : $a; }
   
   ?>

See also `Null Coalescing Operator <https://www.php.net/manual/en/language.operators.comparison.php#language.operators.comparison.coalesce>`_ and `Ternary Operator <https://www.php.net/manual/en/language.operators.comparison.php#language.operators.comparison.ternary>`_.


Suggestions
___________

* Drop the reference at assignation time
* Drop the reference in the argument definition
* Drop the reference in the function return definition




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/NoReferenceForTernary                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.8                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | class                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phpadsnew-php-noreferenceforternary`                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


