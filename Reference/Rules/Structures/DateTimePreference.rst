.. _structures-datetimepreference:

.. _date()-versus-datetime-preference:

date() versus DateTime Preference
+++++++++++++++++++++++++++++++++

.. meta::
	:description:
		date() versus DateTime Preference: Processing dates is done with date() functions or DateTime classes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: date() versus DateTime Preference
	:twitter:description: date() versus DateTime Preference: Processing dates is done with date() functions or DateTime classes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: date() versus DateTime Preference
	:og:type: article
	:og:description: Processing dates is done with date() functions or DateTime classes
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/DateTimePreference.html
	:og:locale: en
Processing dates is done with `date() <https://www.php.net/date>`_ functions or `DateTime <https://www.php.net/`datetime <https://www.php.net/datetime>`_>`_ classes. 

In the `date() <https://www.php.net/date>`_ team, there are the following functions : `date() <https://www.php.net/date>`_, `time() <https://www.php.net/time>`_, `getdate() <https://www.php.net/getdate>`_, `localtime() <https://www.php.net/localtime>`_, `strtotime() <https://www.php.net/strtotime>`_, `strptime() <https://www.php.net/strptime>`_, `gmdate() <https://www.php.net/gmdate>`_, `strftime() <https://www.php.net/strftime>`_, `mktime() <https://www.php.net/mktime>`_, gmktime().

In the `DateTime <https://www.php.net/`datetime <https://www.php.net/datetime>`_>`_ team, there are the instantiation of `DateTime <https://www.php.net/`datetime <https://www.php.net/datetime>`_>`_ and `DateTimeImmutable <https://www.php.net/`datetimeimmutable <https://www.php.net/datetimeimmutable>`_>`_; the DateTime\:\:createFromInterface(), `DateTime\:\:createFromFormat() <https://www.php.net/manual/en/datetime.createfromformat.php>`_, DateTime\:\:createFromImmutable() and DateTime\:\:createFromMutable(). 

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make them all the same.

.. code-block:: php
   
   <?php
   
   // be consistent
   $date = date();
   $time = time();
   $date = date();
   $time = time();
   $date = date();
   $time = time();
   $date = date();
   $time = time();
   $date = date();
   $time = time();
   $date = date();
   $time = time();
   
   // Be consistent, always use the same. 
   $date = new DateTime();
   
   ?>
Connex PHP features
-------------------

  + `date <https://php-dictionary.readthedocs.io/en/latest/dictionary/date.ini.html>`_


Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DateTimePreference                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.9                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+


