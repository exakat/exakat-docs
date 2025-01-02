.. _report-stubs:

Stubs
+++++

Stubs
_____

.. meta::
	:description:
		Stubs: Stubs produces a skeleton from the source code, with all defined structures : constants, functions, classes, interfaces, traits and namespaces. .
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Stubs
	:twitter:description: Stubs: Stubs produces a skeleton from the source code, with all defined structures : constants, functions, classes, interfaces, traits and namespaces. 
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Stubs
	:og:type: article
	:og:description: Stubs produces a skeleton from the source code, with all defined structures : constants, functions, classes, interfaces, traits and namespaces. 
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Reports/.html
	:og:locale: en

Stubs produces a skeleton from the source code, with all defined structures : constants, functions, classes, interfaces, traits and namespaces. 

Stubs takes the original code, and export all defined structures (constants, functions, classes, interfaces, traits and namespaces) in a single and compilable PHP file.

This is convenient for tools that requires documentations for completion, such as IDE.

Constants are exported with their values, properties too. Methods hold their full signature. 

The resulting report is in one file, called `stubs.php`.

.. image:: ../images/report.stubs.png
    :alt: Example of a Stubs report (0)

Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | Stubs                                                            |
+--------------+------------------------------------------------------------------+
| Rulesets     | Stubs doesn't depend on rulesets.                                |
|              |                                                                  |
|              |                                                                  |
+--------------+------------------------------------------------------------------+
| Type         | PHP                                                              |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'stubs.php'.                           |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


