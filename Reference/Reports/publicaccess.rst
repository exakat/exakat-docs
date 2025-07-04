.. _report-publicaccess:

PublicAccess
++++++++++++

PublicAccess
____________

.. meta::
	:description:
		PublicAccess: This report is a map on how to access private methods from public methods..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PublicAccess
	:twitter:description: PublicAccess: This report is a map on how to access private methods from public methods.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PublicAccess
	:og:type: article
	:og:description: This report is a map on how to access private methods from public methods.
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Reports/.html
	:og:locale: en

This report is a map on how to access private methods from public methods.

The Public Access report displays a map that show how to reach private methods by calling.

Public methods are in green, protected methods are in orange and private methods are in red. 

When creating tests for a class, it is often difficult to find the various ways to hit a private method, and, as such, test it. 

This map is built by find all internal calls within a class. Those calls are not systematically made, as conditions may apply. Yet, the map show all possible ways to reach a method, starting from a public one. 

Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | PublicAccess                                                     |
+--------------+------------------------------------------------------------------+
| Rulesets     | PublicAccess doesn't depend on rulesets.                         |
|              |                                                                  |
|              |                                                                  |
+--------------+------------------------------------------------------------------+
| Type         | Dot                                                              |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'exakat.publicaccess'.                 |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


