.. _structures-multilineexpressions:

.. _multiline-expressions:

Multiline Expressions
+++++++++++++++++++++

  List of expressions that are spread across several lines. The default is 2.

Structures that commonly accept several lines, like `match() <https://www.php.net/manual/en/control-structures.match.php>`_, `switch() <https://www.php.net/manual/en/control-structures.switch.php>`_, classes, functions, closures, constant definitions, etc. are omitted. 

Multiline expressions, like complex expressions, tend to be less readable. Although, some multiline expressions are written to make them more readable, compared to a one-line complex expression.


.. code-block:: php
   
   <?php
   
   // foo is not reported for the multiline expression
   function foo() {
   	// this echo is reported
   	echo $a .
   		 $b .
   		 $c;
   } 
   
   
   ?>

+------+---------+---------+-----------------------------------------------------+
| Name | Default | Type    | Description                                         |
+------+---------+---------+-----------------------------------------------------+
| min  | 2       | integer | Minimal number of lines in an expression to report. |
+------+---------+---------+-----------------------------------------------------+



Suggestions
___________

* Reduce the size of the expression by moving it to a method
* Reduce the size of the expression by splitting it into several ones




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MultilineExpressions                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`too-complex-expression`                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


