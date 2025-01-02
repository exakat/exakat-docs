.. _php-isnullvsequalnull:

.. _use-===-null:

Use === null
++++++++++++

.. meta::
	:description:
		Use === null: It is faster to use === null than the function is_null().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use === null
	:twitter:description: Use === null: It is faster to use === null than the function is_null()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use === null
	:og:type: article
	:og:description: It is faster to use === null than the function is_null()
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use === null.html
	:og:locale: en
It is faster to use === null than the function `is_null() <https://www.php.net/is_null>`_.
This is a micro-optimisation. And being used frequently, and in loops, it may yield visible speed up.

.. code-block:: php
   
   <?php
   
   // Operator === is faster
   if ($a === null) {
   
   }
   
   // Function call is slow 
   if (is_null($a)) {
   
   }
   ?>

See also `is_null <https://www.php.net/is_null>`_.

Connex PHP features
-------------------

  + `strict-comparison <https://php-dictionary.readthedocs.io/en/latest/dictionary/strict-comparison.ini.html>`_
  + `null <https://php-dictionary.readthedocs.io/en/latest/dictionary/null.ini.html>`_


Suggestions
___________

* Use === comparison instead of is_null




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/IsnullVsEqualNull                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`php-cs-fixable <ruleset-php-cs-fixable>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `avoid-those-slow-functions <https://github.com/dseguy/clearPHP/tree/master/rules/avoid-those-slow-functions.md>`__                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


