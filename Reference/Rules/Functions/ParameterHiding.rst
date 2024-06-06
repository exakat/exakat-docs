.. _functions-parameterhiding:

.. _parameter-hiding:

Parameter Hiding
++++++++++++++++

  When a parameter is set to another variable, and never used.

While this is a legit syntax, parameter hiding tends to make the code confusing. The parameter itself seems to be unused, while some extra variable appears.

Keep this code simple by removing the hiding parameter.

.. code-block:: php
   
   <?php
   
   function substract($a, $b) {
       // $b is given to $c;
       $c = $b; 
   
       // $c is used, but $b would be the same
       return $a - $c;
   }
   
   ?>

Suggestions
___________

* Remove the parameter alias and use the parameter
* Add some modifications to the alias parameter and use it




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/ParameterHiding                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | parameter                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


