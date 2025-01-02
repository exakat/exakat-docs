.. _report-file-dependendies-html:

File dependendies HTML
++++++++++++++++++++++

File dependendies HTML
______________________

.. meta::
	:description:
		File dependendies HTML: This reports displays the file dependencies, based on definition usages..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: File dependendies HTML
	:twitter:description: File dependendies HTML: This reports displays the file dependencies, based on definition usages.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: File dependendies HTML
	:og:type: article
	:og:description: This reports displays the file dependencies, based on definition usages.
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Reports/.html
	:og:locale: en

This reports displays the file dependencies, based on definition usages.

This report displays all dependencies between files. A file depends on another when it makes usage of one of its definitions : constant, functions, classes, traits, interfaces. 

For example, `A.php` depends on `B.php`, because `A.php` uses the function `foo`, which is defined in the `B.php` file. On the other hand, `B.php` doesn't depends on `A.php`, as a function may be defined, but not used. 

This diagram shows which files may be used without others.

The resulting diagram is in HTML file, which is readable with most browsers, from a web server. 

Warning : for browser security reasons, the report will NOT load as a local file. It needs to be served by an HTTP server, so all resources are correctly located.

Warning : large applications (> 1000 files) will require a lot of resources to open.

Another version of the same diagram is called Filedependencies, and produces a DOT file

.. image:: ../images/report.filedependencieshtml.png
    :alt: Example of a File dependendies HTML report (0)

Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | File dependendies HTML                                           |
+--------------+------------------------------------------------------------------+
| Rulesets     | This reports works with an arbitrary list of results.            |
|              |                                                                  |
|              |                                                                  |
+--------------+------------------------------------------------------------------+
| Type         | HTML                                                             |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'dependencies'.                        |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


