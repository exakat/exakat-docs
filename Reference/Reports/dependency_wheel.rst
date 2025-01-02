.. _report-dependency-wheel:

Dependency Wheel
++++++++++++++++

Dependency Wheel
________________

.. meta::
	:description:
		Dependency Wheel: The DependencyWheel represents dependencies in a code source..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Dependency Wheel
	:twitter:description: Dependency Wheel: The DependencyWheel represents dependencies in a code source.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Dependency Wheel
	:og:type: article
	:og:description: The DependencyWheel represents dependencies in a code source.
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Reports/.html
	:og:locale: en

The DependencyWheel represents dependencies in a code source.

Dependency Wheel is a javascript visualization of the classes dependencies in the code. Every class, interface and trait are represented as a circle, and every relation between the classes are represented by a link between them, inside the circle. 

It is based on Francois Zaninotto's `DependencyWheel <http://fzaninotto.github.com/DependencyWheel>`_ and the `d3.js <https://github.com/mbostock/d3>`_.

.. image:: ../images/report.dependencywheel.png
    :alt: Example of a Dependency Wheel report (0)

Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | Dependency Wheel                                                 |
+--------------+------------------------------------------------------------------+
| Rulesets     | Dependency Wheel doesn't depend on rulesets.                     |
|              |                                                                  |
|              |                                                                  |
+--------------+------------------------------------------------------------------+
| Type         | HTML                                                             |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'wheel'.                               |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


