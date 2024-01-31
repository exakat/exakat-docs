.. _structures-dontaddseconds:

.. _don't-add-seconds:

Don't Add Seconds
+++++++++++++++++

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


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DontAddSeconds                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
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
| Features     | date                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


