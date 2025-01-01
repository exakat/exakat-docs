.. _structures-echowithconcat:

.. _echo-with-concat:

Echo With Concat
++++++++++++++++

.. meta::
	:description:
		Echo With Concat: Optimize your ``echo``'s by avoiding concatenating at ``echo`` time, but serving all argument separated.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Echo With Concat
	:twitter:description: Echo With Concat: Optimize your ``echo``'s by avoiding concatenating at ``echo`` time, but serving all argument separated
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Echo With Concat
	:og:type: article
	:og:description: Optimize your ``echo``'s by avoiding concatenating at ``echo`` time, but serving all argument separated
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/EchoWithConcat.html
	:og:locale: en
Optimize your ``echo``'s by avoiding concatenating at ``echo`` time, but serving all argument separated. This will save PHP a memory copy.

If values, literals and variables, are small enough, this won't have visible impact. Otherwise, this is less work and less memory waste.
instead of
It is a micro-optimisation.

.. code-block:: php
   
   <?php
     echo $a, ' b ', $c;
   ?>
Connex PHP features
-------------------

  + `echo <https://php-dictionary.readthedocs.io/en/latest/dictionary/echo.ini.html>`_


Suggestions
___________

* Turn the concatenation into a list of argument, by replacing the dots by commas.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/EchoWithConcat                                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-unnecessary-string-concatenation <https://github.com/dseguy/clearPHP/tree/master/rules/no-unnecessary-string-concatenation.md>`__                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phpdocumentor-structures-echowithconcat`, :ref:`case-teampass-structures-echowithconcat`                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


