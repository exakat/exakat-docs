.. _structures-invaliddatescanningformat:

.. _invalid-date-scanning-format:

Invalid Date Scanning Format
++++++++++++++++++++++++++++

  The format string used with `Datetime\:\:createFromFormat() <https://www.php.net/manual/en/datetime.createfromformat.php>`_ method (or similar) contains unknown characters. 

This won't raise an `error <https://www.php.net/error>`_, though the resulting values should be checked.

.. code-block:: php
   
   <?php
   
   // format is valid
   $date = datetimeimmutable::createFromFormat('d/m/Y', $a);
   // When wrong, $date is false
   // The errors are in datetimeimmutable::getLastErrors();
   
   // X is not a valid character for 
   $date = datetimeimmutable::createFromFormat('d/X/Y', $a);
   
   ?>

Suggestions
___________

* Remove the unknown characters
* Replace the unknown character with the expected one




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/InvalidDateScanningFormat                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | date, external-format                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


