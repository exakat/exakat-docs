.. _variables-variableusedonce:

.. _used-once-variables:

Used Once Variables
+++++++++++++++++++

.. meta::
	:description:
		Used Once Variables: This is the list of used once variables.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Used Once Variables
	:twitter:description: Used Once Variables: This is the list of used once variables
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Used Once Variables
	:og:type: article
	:og:description: This is the list of used once variables
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Variables/VariableUsedOnce.html
	:og:locale: en
This is the list of used once variables. 
Such variables are useless. Variables must be used at least twice : once for writing, once for reading, at least. It is recommended to remove them.

In special situations, variables may be used once : 

+ PHP predefined variables, as they are already initialized. They are omitted in this analyze.
+ Interface function's arguments, since the function has no body; They are omitted in this analyze.
+ Dynamically created variables ($$x, ${`$this <https://www.php.net/manual/en/language.oop5.basic.php>`_->y} or also using extract), as they are runtime values and can't be determined at `static <https://www.php.net/manual/en/language.oop5.static.php>`_ code time. They are reported for manual review.
+ Dynamically included files will provide in-scope extra variables.

This rule counts variables at the application level, and not at a method scope level.

.. code-block:: php
   
   <?php
   
   // The variables below never appear again in the code
   $writtenOnce = 1;
   
   foo($readOnce);
   
   ?>

See also `class <https://www.php.net/manual/en/language.oop5.basic.php#language.oop5.basic.class>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Remove the variable
* Fix the name of variable
* Use the variable a second time, at least




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/VariableUsedOnce                                                                                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                             |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                         |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-shopware-variables-variableusedonce`, :ref:`case-vanilla-variables-variableusedonce`                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+


