.. _report-topology-order:

Topology Order
++++++++++++++

Topology Order
______________

.. meta::
	:description:
		Topology Order: This represents a topological order in the code..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Topology Order
	:twitter:description: Topology Order: This represents a topological order in the code.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Topology Order
	:og:type: article
	:og:description: This represents a topological order in the code.
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Reports/.html
	:og:locale: en

This represents a topological order in the code.

Topology displays all dependencies between code structures. Such dependencies lead to a code hierarchy, which is presented here.

There are currently two topology available:

+ Type Order : it represents the order in which classes are organized, based on argument and return type.
+ New Order : it represents the order in which classes are instantiated, with new.



.. image:: ../images/report.topology.png
    :alt: Example of a Topology Order report (0)

Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | Topology Order                                                   |
+--------------+------------------------------------------------------------------+
| Rulesets     | Topology Order doesn't depend on rulesets.                       |
|              |                                                                  |
|              |                                                                  |
+--------------+------------------------------------------------------------------+
| Type         | DOT                                                              |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'exakat.topology.dot'.                 |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


