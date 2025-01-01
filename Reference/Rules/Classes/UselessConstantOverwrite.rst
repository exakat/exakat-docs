.. _classes-uselessconstantoverwrite:

.. _useless-constant-overwrite:

Useless Constant Overwrite
++++++++++++++++++++++++++

.. meta::
	:description:
		Useless Constant Overwrite: A class constant is defined in a parent and child class, with the same value.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless Constant Overwrite
	:twitter:description: Useless Constant Overwrite: A class constant is defined in a parent and child class, with the same value
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless Constant Overwrite
	:og:type: article
	:og:description: A class constant is defined in a parent and child class, with the same value
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/UselessConstantOverwrite.html
	:og:locale: en
A class constant is defined in a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ and child class, with the same value. One of them is useless and may be removed.

.. code-block:: php
   
   <?php
   
   class x {
   	const A = 1;
   	const B = 1;
   }
   
   class y extends x {
   	// A is the same as in the parent class.
   	const A = 1;
   	// B has a new value, so it is important.
   	const B = 2;
   }
   
   ?>

Suggestions
___________

* Remove the parent constant
* Remove the child constant




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UselessConstantOverwrite                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


