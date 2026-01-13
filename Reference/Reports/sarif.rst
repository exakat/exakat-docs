.. _report-sarif:

Sarif
+++++

Sarif
_____

The SARIF report publishes the results in SARIF format.

`Static Analysis Results Interchange Format (SARIF) <https://docs.oasis-open.org/sarif/sarif/v2.0/sarif-v2.0.html>`_  a standard format for the output of static analysis tools. The format is referred to as the “Static Analysis Results Interchange Format” and is abbreviated as SARIF. 

SARIF is a flexible JSON format, that describes in details the rules, the issues and their context.

More details are available at `sarifweb <https://sarifweb.azurewebsites.net/>`_ and `SARIF support for code scanning <https://docs.github.com/en/github/finding-security-vulnerabilities-and-errors-in-your-code/sarif-support-for-code-scanning>`_ at Github.



.. image:: ../images/report.sarif.png
    :alt: Example of a Sarif report (0)

Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Sarif                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | This reports works with an arbitrary list of results.                                                                            |
|              |                                                                                                                                  |
|              |                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------+
| Type         | Json                                                                                                                             |
+--------------+----------------------------------------------------------------------------------------------------------------------------------+
| Target       | This report is written in 'exakat.json'.                                                                                         |
+--------------+----------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_ |
+--------------+----------------------------------------------------------------------------------------------------------------------------------+


