.. _structures-datetimepreference:

.. _date()-versus-datetime-preference:

date() versus DateTime Preference
+++++++++++++++++++++++++++++++++

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
| Features     | date                                                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+


