.. _report-history:

History
+++++++

History
_______

.. meta::
	:description:
		History: The History report collects meta information between audits. It saves the values from the current audit into a separate 'history.sqlite' database..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: History
	:twitter:description: History: The History report collects meta information between audits. It saves the values from the current audit into a separate 'history.sqlite' database.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: History
	:og:type: article
	:og:description: The History report collects meta information between audits. It saves the values from the current audit into a separate 'history.sqlite' database.
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Reports/.html
	:og:locale: en

The History report collects meta information between audits. It saves the values from the current audit into a separate 'history.sqlite' database.

The history tables are the same as the dump.sqlite tables, except for the extra 'serial' table. Each audit comes with 3 identifiers : 

+ 'dump_timestamp' : this is a timmestamp taken when the dump was build
+ 'dump_serial'    : this is a serial number, based on the previous audit, and incremented by one. This is handy to keep the values in sequence
+ 'dump_id'        : this is a unique random id, which helps distinguish audits which may have inconsistency between serial or timestamp.

This report provides a 'history.sqlite' database. The following tables are inventoried : 

+ hash 
+ resultsCounts


Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | History                                                          |
+--------------+------------------------------------------------------------------+
| Rulesets     | This reports works with an arbitrary list of results.            |
|              |                                                                  |
|              |                                                                  |
+--------------+------------------------------------------------------------------+
| Type         | Sqlite                                                           |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'history.sqlite'.                      |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


