.. _constants-constantusedonce:

.. _constant-used-only-once:

Constant Used Only Once
+++++++++++++++++++++++

.. meta::
	:description:
		Constant Used Only Once: This rule reports constants that are used only once.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Constant Used Only Once
	:twitter:description: Constant Used Only Once: This rule reports constants that are used only once
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Constant Used Only Once
	:og:type: article
	:og:description: This rule reports constants that are used only once
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Constant Used Only Once.html
	:og:locale: en
This rule reports constants that are used only once. Constants that are used only once may be replaced by they literal value, unless future use is expected.

This rule works on global and class constants.

.. code-block:: php
   
   <?php
   
   const ONCE = 1;
   
   echo ONCE;
   
   ?>
Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Suggestions
___________

* Use the constant more than once.
* Replace the constant with a literal value.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/ConstantUsedOnce                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


