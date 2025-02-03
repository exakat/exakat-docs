.. _structures-dontaddseconds:


.. _don't-add-seconds:

Don't Add Seconds
+++++++++++++++++

.. meta::
	:description:
		Don't Add Seconds: Avoid adding seconds to a date, and use ``DateTime::modify`` to add an interval.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Don't Add Seconds
	:twitter:description: Don't Add Seconds: Avoid adding seconds to a date, and use ``DateTime::modify`` to add an interval
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Don't Add Seconds
	:og:type: article
	:og:description: Avoid adding seconds to a date, and use ``DateTime::modify`` to add an interval
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Don't Add Seconds.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/DontAddSeconds.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/DontAddSeconds.html","name":"Don't Add Seconds","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Avoid adding seconds to a date, and use ``DateTime::modify`` to add an interval","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Don't Add Seconds.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Avoid adding seconds to a date, and use ``DateTime\:\:modify`` to add an interval. 

This method will handle situations like daylight savings, leap seconds and even leap days.

.. code-block:: php
   
   <?php
   
   // Tomorrow, same time 
   $tomorrow = new DateTime('now')->modify('+1 day');
   
   // Tomorrow, but may be not at the same hour
   $tomorrow = date('now') + 86400;
   
   ?>

See also `DateTime::modify <https://www.php.net/manual/fr/datetimeimmutable.modify.php>`_ and `datetime <https://www.php.net/manual/fr/intro.datetime.php>`_.

Connex PHP features
-------------------

  + `date <https://php-dictionary.readthedocs.io/en/latest/dictionary/date.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DontAddSeconds                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


