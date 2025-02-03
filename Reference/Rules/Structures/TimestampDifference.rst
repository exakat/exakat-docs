.. _structures-timestampdifference:

.. _timestamp-difference:

Timestamp Difference
++++++++++++++++++++

.. meta::
	:description:
		Timestamp Difference: Avoid adding or subtracting quantities of seconds to measure time.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Timestamp Difference
	:twitter:description: Timestamp Difference: Avoid adding or subtracting quantities of seconds to measure time
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Timestamp Difference
	:og:type: article
	:og:description: Avoid adding or subtracting quantities of seconds to measure time
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Timestamp Difference.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/TimestampDifference.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/TimestampDifference.html","name":"Timestamp Difference","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Avoid adding or subtracting quantities of seconds to measure time","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Timestamp Difference.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Avoid adding or subtracting quantities of seconds to measure time. 

``time()``, ``microtime()`` or ``DateTime\:\:format('U')`` provide timestamps, which are the number of seconds since ``January, 1rst, 1970``. They shouldn't be used to calculate duration or another date by adding an amount of seconds. 

Those functions are subject to variations, depending on system clock variations, such as daylight saving time difference (every spring and fall, one hour variation), or leap seconds, happening on ``June, 30th`` or ``December 31th``, as announced by `IERS <https://www.iers.org/IERS/EN/Home/home_node.html>`_.
When the difference may be rounded to a larger time unit (rounding the difference to days, or several hours), the variation may be ignored safely.

When the difference is very small, it requires a better way to measure time difference, such as `Ticks <https://www.php.net/manual/en/control-structures.declare.php#control-structures.declare.ticks>'_, 
`ext/hrtime <https://www.php.net/manual/en/book.hrtime.php>'_, or including a check on the actual time zone (``ini_get()`` with 'date.timezone').

.. code-block:: php
   
   <?php
   
   // Calculating tomorow, same hour, the wrong way
   // tomorrow is not always in 86400s, especially in countries with daylight saving 
   $tomorrow = time()  + 86400; 
   
   // Good way to calculate tomorrow
   $datetime = new DateTime('tomorrow');
   
   ?>

See also `PHP DateTime difference – it’s a trap! <http://blog.codebusters.pl/en/php-datetime-difference-trap/>`_ and `PHP Daylight savings bug? <https://stackoverflow.com/questions/22519091/php-daylight-savings-bug>`_.

Connex PHP features
-------------------

  + `date <https://php-dictionary.readthedocs.io/en/latest/dictionary/date.ini.html>`_


Suggestions
___________

* For small time intervals, use hrtime() functions
* For larger time intervals, use add() method with ``DateTime``




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/TimestampDifference                                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zurmo-structures-timestampdifference`, :ref:`case-shopware-structures-timestampdifference`                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


