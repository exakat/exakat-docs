.. _structures-resultmaybemissing:

.. _results-may-be-missing:

Results May Be Missing
++++++++++++++++++++++

.. meta::
	:description:
		Results May Be Missing: preg_match() may return empty values, if the search fails.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Results May Be Missing
	:twitter:description: Results May Be Missing: preg_match() may return empty values, if the search fails
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Results May Be Missing
	:og:type: article
	:og:description: preg_match() may return empty values, if the search fails
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Results May Be Missing.html
	:og:locale: en
`preg_match() <https://www.php.net/preg_match>`_ may return empty values, if the search fails. It is important to check for the existence of results before assigning them to another variable, or using it.
Since PHP 7.2, it is possible to use the ``PREG_UNMATCHED_AS_NULL`` constant in the flag parameter to avoid this.

.. code-block:: php
   
   <?php
       preg_match('/PHP ([0-9\.]+) /', $res, $r);
       $s = $r[1];
       // $s may end up null if preg_match fails.
   ?>

Suggestions
___________

* Use a final always capturing parenthesis to avoid this
* Use the ``PREG_UNMATCHED_AS_NULL`` option (PHP 7.2)




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ResultMayBeMissing                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


