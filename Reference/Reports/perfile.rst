.. _report-perfile:

Perfile
+++++++

Perfile
_______

.. meta::
	:description:
		Perfile: The Perfile report lays out the results file per file..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Perfile
	:twitter:description: Perfile: The Perfile report lays out the results file per file.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Perfile
	:og:type: article
	:og:description: The Perfile report lays out the results file per file.
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Reports/.html
	:og:locale: en

The Perfile report lays out the results file per file.

The Perfile report displays one result per line, grouped by file, and ordered by line number. Here is an example : 

::
    
   /path/from/project/root/to/file:line[space]name of analysis
   
   
This format is fast, and fitted for human review.



::

    ---------------------------------------------------------
     line  /themes/Rozier/Controllers/LoginController.php
    ---------------------------------------------------------
       34  Multiple Alias Definitions 
       36  Unresolved Use 
       43  Multiple Alias Definitions 
       51  Class Could Be Final 
       58  Undefined Interfaces 
       81  Undefined Interfaces 
       81  Unused Arguments 
       81  Used Once Variables (In Scope) 
       91  Undefined Interfaces 
       91  Unused Arguments 
       91  Used Once Variables (In Scope) 
      101  Undefined Interfaces 
      103  Nested Ifthen 
      104  Unresolved Classes 
      106  Buried Assignation 
      106  Iffectations 
      106  Use Positive Condition 
      121  Uncaught Exceptions 
      121  Unresolved Classes 
      129  Uncaught Exceptions 
    ---------------------------------------------------------
    

Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Perfile                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | This reports works with an arbitrary list of results.                                                                            |
|              |                                                                                                                                  |
|              |                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------+
| Type         | Text                                                                                                                             |
+--------------+----------------------------------------------------------------------------------------------------------------------------------+
| Target       | This report is written in 'stdout'.                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_ |
+--------------+----------------------------------------------------------------------------------------------------------------------------------+


