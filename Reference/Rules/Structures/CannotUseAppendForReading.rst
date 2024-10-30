.. _structures-cannotuseappendforreading:

.. _cannot-use-append-for-reading:

Cannot Use Append For Reading
+++++++++++++++++++++++++++++

  The append operator ``[]`` is used to add a value to an array. It doesn't provide an existing value to read. Hence, the short assignement operators, or the increment ones should not be used with the append operator. For example, the coalesce operator yields an `error <https://www.php.net/error>`_ when used with append.

.. code-block:: php
   
   <?php
   
   $x = [];
   $x[] = 1; // normal usage
   $x[] += 2; // adds a 2, but should yield an error
   $x[]++;    // adds a 1, but should yield an error
   // variations with -= *= &= etc.
   
   $x[] ??= 4; // yields a fatal error
   
   ?>
Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Cannot+use+%5B%5D+for+reading.html>`_




Suggestions
___________

* Remove the short assignement and build a real expression on the right hand of the assignement to append




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CannotUseAppendForReading                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


