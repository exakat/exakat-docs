.. _extensions-extcalendar:

.. _ext-calendar:

ext/calendar
++++++++++++

.. meta\:\:
	:description:
		ext/calendar: Extension ext/calendar.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/calendar
	:twitter:description: ext/calendar: Extension ext/calendar
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/calendar
	:og:type: article
	:og:description: Extension ext/calendar
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extcalendar.html
	:og:locale: en
  Extension ext/calendar.

The calendar extension presents a series of functions to simplify converting between different calendar formats.

.. code-block:: php
   
   <?php
   $number = cal_days_in_month(CAL_GREGORIAN, 8, 2003); // 31
   echo "There were {$number} days in August 2003";
   ?>

See also `Calendar Functions <http://www.php.net/manual/en/ref.calendar.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extcalendar                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


