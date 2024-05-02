.. _structures-nextmonthtrap:

.. _next-month-trap:

Next Month Trap
+++++++++++++++

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


Suggestions
___________

* Review strtotime() usage for month additions
* Base your calculations for the next/previous months on the first day of the month (or any day before the 28th)
* Avoid using '+n month' with Datetime() after the 28th of any month (sic)




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NextMonthTrap                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Top10 <ruleset-Top10>`                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.1                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | date                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-contao-structures-nextmonthtrap`, :ref:`case-edusoho-structures-nextmonthtrap`                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


