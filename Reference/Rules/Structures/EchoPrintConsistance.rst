.. _structures-echoprintconsistance:

.. _echo-or-print:

Echo Or Print
+++++++++++++

  Echo and print have the same functional use. <?= and `printf() <https://www.php.net/printf>`_ are also considered in this analysis. 

There seems to be a choice that is not enforced : one form is dominant, (> 90%) while the others are rare. 

The analyzed code has less than 10% of one of the three : for consistency reasons, it is recommended to make them all the same. 

It happens that print, echo or <?= are used depending on coding style and files. One file may be consistently using print, while the others are all using echo.

.. code-block:: php
   
   <?php
   
   echo 'a';
   echo 'b';
   echo 'c';
   echo 'd';
   echo 'e';
   echo 'f';
   echo 'g';
   echo 'h';
   echo 'i';
   echo 'j';
   echo 'k';
   
   // This should probably be written 'echo';
   print 'l';
   
   ?>
Connex PHP features
-------------------

  + `echo <https://php-dictionary.readthedocs.io/en/latest/dictionary/echo.ini.html>`_
  + `print <https://php-dictionary.readthedocs.io/en/latest/dictionary/print.ini.html>`_


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/EchoPrintConsistance                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Coding conventions <ruleset-Coding-conventions>`, :ref:`Preferences <ruleset-Preferences>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


