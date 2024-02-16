.. _report-text:

Text
++++

Text
____

The Text report is a very simple text format.

The Text report displays one result per line, with the following format  : 

::
    
   /path/from/project/root/to/file:line[space]name of analysis
   
   
This format is fast, and fitted for machine communications.



::

    /classes/test.php:1002	Php/ShouldUseFunction	Should Use Function	array_values(array_unique(array_merge($classTags, $annotations['tags'])))
    /classes/test.php:1002	Php/ShouldUseFunction	Should Use Function	array_merge($classTags, $annotations['tags'])
    /classes/test.php:1005	Structures/NoArrayUnique	Avoid array_unique()	array_unique(array_merge($classTags, $this->testMethods[$testMethodName]['tags']))
    /classes/test.php:1005	Performances/SlowFunctions	Slow Functions	array_unique(array_merge($classTags, $this->testMethods[$testMethodName]['tags']))
    

Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Text                                                                                                                             |
+--------------+----------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | This reports works with an arbitrary list of results.                                                                            |
|              |                                                                                                                                  |
|              |                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------+
| Type         | Text                                                                                                                             |
+--------------+----------------------------------------------------------------------------------------------------------------------------------+
| Target       | This report is written to the standard output.                                                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_ |
+--------------+----------------------------------------------------------------------------------------------------------------------------------+


