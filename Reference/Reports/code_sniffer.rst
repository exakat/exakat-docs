.. _report-code-sniffer:

Code Sniffer
++++++++++++

Code Sniffer
____________

The CodeSniffer report exports in the CodeSniffer format.

This format reports analysis using the Codesniffer's result format. 

See also `Code Sniffer Report <https://github.com/squizlabs/PHP_CodeSniffer/wiki/Reporting>`_.


::

    FILE : /Path/To/View/The/File.php
    --------------------------------------------------------------------------------
    FOUND 3 ISSUES AFFECTING 3 LINES
    --------------------------------------------------------------------------------
     32 | MINOR | Could Use Alias
     41 | MINOR | Could Make A Function
     43 | MINOR | Could Make A Function
    --------------------------------------------------------------------------------
    

Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | Code Sniffer                                                     |
+--------------+------------------------------------------------------------------+
| Rulesets     | This reports works with an arbitrary list of results.            |
|              |                                                                  |
|              |                                                                  |
+--------------+------------------------------------------------------------------+
| Type         | TEXT                                                             |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'exakat.txt'.                          |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


