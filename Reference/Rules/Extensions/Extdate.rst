.. _extensions-extdate:

.. _ext-date:

ext/date
++++++++

.. meta\:\:
	:description:
		ext/date: Extension ext/date.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/date
	:twitter:description: ext/date: Extension ext/date
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/date
	:og:type: article
	:og:description: Extension ext/date
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extdate.html
	:og:locale: en
  Extension ext/date.

These functions allows the manipulation of date and time from the server where the PHP scripts are running.

.. code-block:: php
   
   <?php
   $dt = new DateTime('2015-11-01 00:00:00', new DateTimeZone('America/New_York'));
   echo 'Start: ', $dt->format('Y-m-d H:i:s P'), PHP_EOL;
   $dt->add(new DateInterval('PT3H'));
   echo 'End:   ', $dt->format('Y-m-d H:i:s P'), PHP_EOL;
   ?>

See also `Date and Time <https://www.php.net/manual/en/book.datetime.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extdate                                                                                                                                                                      |
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


