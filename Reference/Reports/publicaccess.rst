.. _report-publicaccess:

PublicAccess
++++++++++++

PublicAccess
____________

This report is a map on how to access private methods from public methods.

The Public Access report displays a map that show how to reach private methods by calling.

Public methods are in green, protected methods are in orange and private methods are in red. 

When creating tests for a class, it is often difficult to find the various ways to hit a private method, and, as such, test it. 

This map is built by find all internal calls within a class. Those calls are not systematically made, as conditions may apply. Yet, the map show all possible ways to reach a method, starting from a public one. 

.. image:: ../images/publicaccess.png
    :alt: Example of a PublicAccess report (0)

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


