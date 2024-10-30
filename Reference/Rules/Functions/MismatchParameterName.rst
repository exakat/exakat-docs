.. _functions-mismatchparametername:

.. _mismatch-parameter-name:

Mismatch Parameter Name
+++++++++++++++++++++++

  Parameter name change in overwritten method. This may lead to errors when using PHP 8.0 named arguments. 

PHP use the name of the parameter in the method whose code is executed. When the name change between the method and the overwritten method, the consistency is broken.

Here is another example, in early PHP 8.0 (courtesy of `Carnage <https://twitter.com/giveupalready>`_).

.. code-block:: php
   
   <?php
   
   class x {
       function getValue($name) {}
   }
   
   class y extends x {
       // consistent with the method above
       function getValue($name) {}
   }
   
   class z extends x {
       // inconsistent with the method above
       function getValue($label) {}
   }
   
   ?>
Connex PHP features
-------------------

  + `named-parameter <https://php-dictionary.readthedocs.io/en/latest/dictionary/named-parameter.ini.html>`_


Suggestions
___________

* Make sure all the names are the same, between methods




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/MismatchParameterName                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.8                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


