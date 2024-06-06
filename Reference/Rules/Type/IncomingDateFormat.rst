.. _type-incomingdateformat:

.. _incoming-date-formats:

Incoming Date Formats
+++++++++++++++++++++

  This is the list of format string used when creating dates. 

This is particularly interesting for relative time strings inventories.
This doesn't collect the dynamical dates, built from strings. `strtotime() <https://www.php.net/strtotime>`_ and date\:\:createFromFormat() are used.

.. code-block:: php
   
   <?php
   
   echo strtotime("now"), "\n";
   
   ?>

See also `DateTimeImmutable::createFromFormat <https://www.php.net/manual/en/datetime.createfromformat.php>`_.


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
| Features     | date-format                                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


