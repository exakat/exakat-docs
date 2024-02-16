.. _report-xml:

Xml
+++

Xml
___

The Xml report exports in XML format.

XML version of the reports. It uses the same format than PHP Code Sniffer to output the results. 


::

    <?xml version="1.0" encoding="UTF-8"?>
    <phpcs version="0.8.6">
    <file name="/src/NlpTools/Stemmers/PorterStemmer.php" errors="0" warnings="105" fixable="0">
     <warning line="55" column="0" source="Php/EllipsisUsage" severity="Major" fixable="0">... Usage</warning>
    

Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | Xml                                                              |
+--------------+------------------------------------------------------------------+
| Rulesets     | This reports works with an arbitrary list of results.            |
|              |                                                                  |
|              |                                                                  |
+--------------+------------------------------------------------------------------+
| Type         | XML                                                              |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'exakat.xml'.                          |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


