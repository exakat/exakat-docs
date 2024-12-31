.. _structures-issetwithconstant:

.. _isset()-with-constant:

isset() With Constant
+++++++++++++++++++++

.. meta\:\:
	:description:
		isset() With Constant: Until PHP 7, it was possible to use arrays as constants, but it was not possible to test them with isset.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: isset() With Constant
	:twitter:description: isset() With Constant: Until PHP 7, it was possible to use arrays as constants, but it was not possible to test them with isset
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: isset() With Constant
	:og:type: article
	:og:description: Until PHP 7, it was possible to use arrays as constants, but it was not possible to test them with isset
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/IssetWithConstant.html
	:og:locale: en
  Until PHP 7, it was possible to use arrays as constants, but it was not possible to test them with `isset <https://www.www.php.net/isset>`_.

This would yield an `error <https://www.php.net/error>`_ : ``Cannot use `isset() <https://www.www.php.net/isset>`_ on the `result <https://www.php.net/result>`_ of an expression (you can use "null !== expression" instead)``. This is a backward incompatibility.

.. code-block:: php
   
   <?php
   const X = [1,2,3];
   
   if (isset(X[4])) {}
   ?>
Related PHP errors 
-------------------

  + `Cannot use isset() on the result of an expression (you can use "null !== expression" instead) <https://php-errors.readthedocs.io/en/latest/messages/cannot-use-isset%5C%28%5C%29-on-the-result-of-an-expression-%5C%28you-can-use-%22null-%5C%21%5C%3D%5C%3D-expression%22-instead%5C%29.html>`_



Connex PHP features
-------------------

  + `isset <https://php-dictionary.readthedocs.io/en/latest/dictionary/isset.ini.html>`_


Suggestions
___________

* Avoid testing values on constants.




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Structures/IssetWithConstant                                                                                                                                                                                                                                                                                 |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                                                                                                                                                                                        |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 7.0 and more recent                                                                                                                                                                                                                                                                                 |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Major                                                                                                                                                                                                                                                                                                        |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Instant (5 mins)                                                                                                                                                                                                                                                                                             |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.0                                                                                                                                                                                                                                                                                                      |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                                                                                                                                                    |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                      |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


