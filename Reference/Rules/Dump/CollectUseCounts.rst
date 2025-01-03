.. _dump-collectusecounts:

.. _collect-use-counts:

Collect Use Counts
++++++++++++++++++

.. meta::
	:description:
		Collect Use Counts: This rule counts the number of ``use``` expression in a file.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Collect Use Counts
	:twitter:description: Collect Use Counts: This rule counts the number of ``use``` expression in a file
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Collect Use Counts
	:og:type: article
	:og:description: This rule counts the number of ``use``` expression in a file
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Collect Use Counts.html
	:og:locale: en
This rule counts the number of ``use``` expression in a file. ``use`` expressions import external classes, interfaces, enums, constant, functions and traits. 

A high number of imports may signal a class that is doing to much.

.. code-block:: php
   
   <?php
   
   // This count 4 uses
   use A as B;
   use F\C, F\D, F\E;
   
   ?>
Connex PHP features
-------------------

  + `use <https://php-dictionary.readthedocs.io/en/latest/dictionary/use.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectUseCounts                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.9                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


