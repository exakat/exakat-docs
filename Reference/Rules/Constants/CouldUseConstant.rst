.. _constants-coulduseconstant:

.. _could-use-existing-constant:

Could Use Existing Constant
+++++++++++++++++++++++++++

  This rule reports literals that have the same value as a constant, and, as such, might be used as a constant, instead of a literal.



Floats are not considered by this rule, for comparison reasons. Also, ``true``, ``false``, ``null``, 0 and 1 are also automatically excluded.

.. code-block:: php
   
   <?php
   
   const A = 1;
   
   $a = 1;
   
   ?>

+---------------+---------+-------+------------------------------------------------------------------------------------------------------------------------+
| Name          | Default | Type  | Description                                                                                                            |
+---------------+---------+-------+------------------------------------------------------------------------------------------------------------------------+
| omittedValues |         | array | Comma-separated list of values that have to be ignored with this analysis. They replace the default values of 0 and 1. |
+---------------+---------+-------+------------------------------------------------------------------------------------------------------------------------+


Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Suggestions
___________

* Use the constant instead of the literal
* Create a new constant for that literal




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/CouldUseConstant                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


