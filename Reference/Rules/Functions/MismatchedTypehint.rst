.. _functions-mismatchedtypehint:

.. _mismatched-typehint:

Mismatched Typehint
+++++++++++++++++++

.. meta::
	:description:
		Mismatched Typehint: Relayed arguments don't have the same typehint.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Mismatched Typehint
	:twitter:description: Mismatched Typehint: Relayed arguments don't have the same typehint
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Mismatched Typehint
	:og:type: article
	:og:description: Relayed arguments don't have the same typehint
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Mismatched Typehint.html
	:og:locale: en
Relayed arguments don't have the same typehint.

Typehint acts as a filter method. When an object is checked with a first class, and then checked again with a second distinct class, the whole process is always false : $a can't be of two different classes at the same time.
Note : This analysis currently doesn't check generalisation of classes : for example, when B is a child of BB, it is still reported as a mismatch.

.. code-block:: php
   
   <?php
   
   // Foo() calls bar()
   function foo(A $a, B $b) {
       bar($a, $b);
   }
   
   // $a is of A typehint in both methods, but 
   // $b is of B then BB typehing
   function bar(A $a, BB $b) {
   
   }
   
   ?>
Connex PHP features
-------------------

  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_


Suggestions
___________

* Ensure that the default value match the expected typehint.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/MismatchedTypehint                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Typechecks <ruleset-Typechecks>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.3                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-functions-mismatchedtypehint`                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+


