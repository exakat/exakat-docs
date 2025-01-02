.. _report-classes-dependendies-html:

Classes dependendies HTML
+++++++++++++++++++++++++

Classes dependendies HTML
_________________________

.. meta::
	:description:
		Classes dependendies HTML: This reports displays the class dependencies, based on definition usages..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Classes dependendies HTML
	:twitter:description: Classes dependendies HTML: This reports displays the class dependencies, based on definition usages.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Classes dependendies HTML
	:og:type: article
	:og:description: This reports displays the class dependencies, based on definition usages.
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Reports/.html
	:og:locale: en

This reports displays the class dependencies, based on definition usages.

This report displays all dependencies between classes, interfaces and traits. A class (or interface or trait) depends on another class (or interface or trait) when it makes usage of one of its definitions : extends, implements, use, and static calls. 

For example, `A` depends on `B`, because `A` extends `B`. 

The resulting diagram is in HTML file, which is readable with most browsers, from a web server. 

Warning : for browser security reasons, the report will NOT load as a local file. It needs to be served by an HTTP server, so all resources are correctly located.

Warning : large applications (> 1000 classes) will require a lot of resources to open.

.. image:: ../images/report.classdependencies.png
    :alt: Example of a Classes dependendies HTML report (0)

Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | Classes dependendies HTML                                        |
+--------------+------------------------------------------------------------------+
| Rulesets     | Classes dependendies HTML doesn't depend on rulesets.            |
|              |                                                                  |
|              |                                                                  |
+--------------+------------------------------------------------------------------+
| Type         | HTML                                                             |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'class_dependencies'.                  |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


