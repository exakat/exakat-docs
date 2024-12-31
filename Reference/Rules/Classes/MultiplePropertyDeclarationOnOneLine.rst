.. _classes-multiplepropertydeclarationononeline:

.. _multiple-property-declaration-on-one-line:

Multiple Property Declaration On One Line
+++++++++++++++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Multiple Property Declaration On One Line: Multiple properties are defined on the same line.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Multiple Property Declaration On One Line
	:twitter:description: Multiple Property Declaration On One Line: Multiple properties are defined on the same line
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Multiple Property Declaration On One Line
	:og:type: article
	:og:description: Multiple properties are defined on the same line
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/MultiplePropertyDeclarationOnOneLine.html
	:og:locale: en
  Multiple properties are defined on the same line. They could be defined independently, on separate expressions.

Keeping properties separate helps documenting and refactoring them independently.

.. code-block:: php
   
   <?php
   
   // multiple definition on one expression
   class point {
       private $x, $y, $z;
   
       // more code
   }
   
   // one line, one definition
   class point2 {
       private $x;
       
       private $y;
       
       private $z;
   
       // more code
   }
   
   ?>

Suggestions
___________

* Split the definitions to one by line




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MultiplePropertyDeclarationOnOneLine                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Coding conventions <ruleset-Coding-conventions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.2                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


