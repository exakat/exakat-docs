.. _dump-collectfilesdependencies:

.. _collect-files-dependencies:

Collect Files Dependencies
++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Collect Files Dependencies: Collect all dependencies between files, based on definitions and usage.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Collect Files Dependencies
	:twitter:description: Collect Files Dependencies: Collect all dependencies between files, based on definitions and usage
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Collect Files Dependencies
	:og:type: article
	:og:description: Collect all dependencies between files, based on definitions and usage
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Dump/CollectFilesDependencies.html
	:og:locale: en
  Collect all dependencies between files, based on definitions and usage.

For example, file `A.php`, which defines de class `A`, is a dependence to a file `B.php`, which makes a call to a method from `A`,  or use `A` as a typehint, etc..

Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectFilesDependencies                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.8                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


