.. _php-dateformats:

.. _date-formats:

Date Formats
++++++++++++

.. meta\:\:
	:description:
		Date Formats: Inventory of date formats used in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Date Formats
	:twitter:description: Date Formats: Inventory of date formats used in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Date Formats
	:og:type: article
	:og:description: Inventory of date formats used in the code
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/DateFormats.html
	:og:locale: en
  Inventory of date formats used in the code. 

Date format are detected with calls to `date() <https://www.php.net/date>`_, `strftime() <https://www.php.net/strftime>`_, `gmstrftime() <https://www.php.net/gmstrftime>`_, `date_format() <https://www.php.net/date_format>`_ functions and to the format() method on ``Datetime`` and ``DatetimeImmutable``.

.. code-block:: php
   
   <?php
   
   $time = time();
   // This is a formated date
   echo date('r', $time);
   
   ?>

See also `Date and Time <https://www.php.net/manual/en/book.datetime.php>`_.

Connex PHP features
-------------------

  + `date <https://php-dictionary.readthedocs.io/en/latest/dictionary/date.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/DateFormats                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Inventory <ruleset-Inventory>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.16                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


