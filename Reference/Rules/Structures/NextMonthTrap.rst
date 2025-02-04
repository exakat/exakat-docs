.. _structures-nextmonthtrap:


.. _next-month-trap:

Next Month Trap
+++++++++++++++

.. meta::
	:description:
		Next Month Trap: Avoid using +1 month with strtotime().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Next Month Trap
	:twitter:description: Next Month Trap: Avoid using +1 month with strtotime()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Next Month Trap
	:og:type: article
	:og:description: Avoid using +1 month with strtotime()
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Next Month Trap.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NextMonthTrap.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NextMonthTrap.html","name":"Next Month Trap","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Avoid using +1 month with strtotime()","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Next Month Trap.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Avoid using +1 month with `strtotime() <https://www.php.net/strtotime>`_. 

`strtotime() <https://www.php.net/strtotime>`_ calculates the next month by incrementing the month number. For day number that do not exist from one month to the next, `strtotime() <https://www.php.net/strtotime>`_ fixes them by setting them in the next-next month. 

This happens to January, March, May, July, August and October. January is also vulnerable for 29 (not every year), 30 and 31. 

To use '+1 month', rely on 'first day of next month' or 'last day of next month' to extract the next month's name. For longer interfaces, start from 'first day of next month'.
Note that ``Datetime`` and ``DatetimeImmutable`` are also subject to the same trap.

.. code-block:: php
   
   <?php
   
   // Base date is October 31 => 10/31
   // +1 month adds +1 to 10 => 11/31 
   // Since November 31rst doesn't exists, it is corrected to 12/01. 
   echo date('F', strtotime('+1 month',mktime(0,0,0,$i,31,2017))).PHP_EOL;
   
   // Base date is October 31 => 10/31
   echo date('F', strtotime('first day of next month',mktime(0,0,0,$i,31,2017))).PHP_EOL;
   
   ?>

See also `It is the 31st again <https://twitter.com/rasmus/status/925431734128197632>`_.

Connex PHP features
-------------------

  + `Dates <https://php-dictionary.readthedocs.io/en/latest/dictionary/date.ini.html>`_


Suggestions
___________

* Review strtotime() usage for month additions
* Base your calculations for the next/previous months on the first day of the month (or any day before the 28th)
* Avoid using '+n month' with Datetime() after the 28th of any month (sic)




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NextMonthTrap                                                                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.1                                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-contao-structures-nextmonthtrap`, :ref:`case-edusoho-structures-nextmonthtrap`                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


