.. _structures-printanddie:

.. _print-and-die:

Print And Die
+++++++++++++

  `Die() <https://www.php.net/die>`_ also prints. 

When stopping a script with `die() <https://www.php.net/die>`_, it is possible to provide a message as first argument, that will be displayed at execution. There is no need to make a specific call to print or echo.

.. code-block:: php
   
   <?php
   
   //  die may do both print and die.
   echo 'Error message';
   die();
   
   //  exit may do both print and die.
   print 'Error message';
   exit;
   
   //  exit cannot print integers only : they will be used as status report to the system.
   print 'Error message';
   exit 1;
   
   ?>
Connex PHP features
-------------------

  + `print <https://php-dictionary.readthedocs.io/en/latest/dictionary/print.ini.html>`_
  + `die <https://php-dictionary.readthedocs.io/en/latest/dictionary/die.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/PrintAndDie                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


