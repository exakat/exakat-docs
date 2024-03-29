.. _extensions-exttaint:

Extensions/Exttaint
+++++++++++++++++++

  Taint is a extension used to detect and track tainted string. It follows each assignation of the code and keeps track of its taint. And also can be used to spot sql injection vulnerabilities, shell inject, etc.

.. code-block:: php
   
   <?php
   $a = trim($_GET['a']);
   
   $file_name = '/tmp' .  $a;
   $output    = "Welcome, {$a} !!!";
   
   //Warning: main() [function.echo]: Attempt to echo a string that might be tainted
   
   ?>

See also `taint <https://www.php.net/manual/en/book.taint.php>`_ and `taint on github <https://github.com/laruence/taint>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Exttaint                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | taint                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


