.. _report-file-dependendies:

File dependendies
+++++++++++++++++

File dependendies
_________________

This reports displays the file dependencies, based on definition usages.

This report displays all dependencies between files. A file depends on another when it makes usage of one of its definitions : constant, functions, classes, traits, interfaces. 

For example, `A.php` depends on `B.php`, because `A.php` uses the function `foo`, which is defined in the `B.php` file. On the other hand, `B.php` doesn't depends on `A.php`, as a function may be defined, but not used. 

This diagram shows which files may be used without others.

The resulting diagram is a DOT file, which is readable with [Graphviz](https://www.graphviz.org/about/). Those viewers will display the diagram, and also convert it to other format, such as PNG, JPEG, PDF or others.  

Another version of the same diagram is called Filedependencieshtml

.. image:: ../images/report.filedependencies.png
    :alt: Example of a File dependendies report (0)

Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | File dependendies                                                |
+--------------+------------------------------------------------------------------+
| Rulesets     | This reports works with an arbitrary list of results.            |
|              |                                                                  |
|              |                                                                  |
+--------------+------------------------------------------------------------------+
| Type         | DOT                                                              |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'dependencies.dot'.                    |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


