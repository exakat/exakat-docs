.. _type-incomingdateformat:

.. _incoming-date-formats:

Incoming Date Formats
+++++++++++++++++++++

.. meta::
	:description:
		Incoming Date Formats: This is the list of format string used when creating dates.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Incoming Date Formats
	:twitter:description: Incoming Date Formats: This is the list of format string used when creating dates
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Incoming Date Formats
	:og:type: article
	:og:description: This is the list of format string used when creating dates
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Incoming Date Formats.html
	:og:locale: en
This is the list of format string used when creating dates. 

This is particularly interesting for relative time strings inventories.
This doesn't collect the dynamical dates, built from strings. `strtotime() <https://www.php.net/strtotime>`_ and date\:\:createFromFormat() are used.

.. code-block:: php
   
   <?php
   
   echo strtotime("now"), "\n";
   
   ?>

See also `DateTimeImmutable::createFromFormat <https://www.php.net/manual/en/datetime.createfromformat.php>`_.

Connex PHP features
-------------------

  + `date-format <https://php-dictionary.readthedocs.io/en/latest/dictionary/date-format.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/IncomingDateFormat                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Inventory <ruleset-Inventory>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


