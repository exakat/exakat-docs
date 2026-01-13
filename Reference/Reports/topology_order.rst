.. _report-topology-order:

Topology Order
++++++++++++++

Topology Order
______________

This represents a topological order in the code.

Topology displays all dependencies between code structures. Such dependencies lead to a code hierarchy, which is presented here.

There are currently two topology available:

+ Typehint Order : it represents the order in which classes are organized, based on argument and return type.
+ New Order : it represents the order in which classes are instantiated, with new.



.. image:: ../images/report.topology.png
    :alt: Example of a Topology Order report (0)

.. image:: ../images/report.topology.typehints.png
    :alt: Example of a Topology Order report (1)

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


