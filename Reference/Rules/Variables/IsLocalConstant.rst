.. _variables-islocalconstant:

.. _variable-is-a-local-constant:

Variable Is A Local Constant
++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Variable Is A Local Constant: A variable that is written once, then never modified : it behaves like a constant.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Variable Is A Local Constant
	:twitter:description: Variable Is A Local Constant: A variable that is written once, then never modified : it behaves like a constant
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Variable Is A Local Constant
	:og:type: article
	:og:description: A variable that is written once, then never modified : it behaves like a constant
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Variables/IsLocalConstant.html
	:og:locale: en
  A variable that is written once, then never modified : it behaves like a constant. Some other rule may take advantage of this.

.. code-block:: php
   
   <?php
   
   function foo() {
       $localConstant = 'Hello';
       echo $localConstant;
   
       $variable = 'Hello, ';
       $variable .= date('r');
       echo $variable;
   }
   
   ?>

Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/IsLocalConstant                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`First <ruleset-First>`, :ref:`NoDoc <ruleset-NoDoc>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.3                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+


