.. _performances-csvinloops:

.. _fputcsv()-in-loops:

fputcsv() In Loops
++++++++++++++++++

  `fputcsv() <https://www.php.net/fputcsv>`_ is slow when called on each row. It actually flushes the data to the disk each time, and that results in a inefficient dump to the disk, each call.

To speed up this process, it is recommended to dump the CSV to memory first, then dump the memory to the disk, in larger chunks. Since `fputcsv() <https://www.php.net/fputcsv>`_ works only on stream, it is necessary to use a memory stream.

The speed improvement is significant on small rows, while it may be less significant on larger rows : with more data in the rows, the file buffer may fill up more efficiently. On small rows, the speed gain is up to 7 times.

.. code-block:: php
   
   <?php
   
   // Speedy yet memory intensive version
   $f = fopen('php://memory', 'w+');
   foreach($data_source as $row) {
       // You may configure fputcsv as usual
       fputcsv($f, $row);
   }
   rewind($f); // Important
   $fp = fopen('final.csv', 'w+');
   fputs($fp, stream_get_contents($f));
   fclose($fp);
   fclose($f);
   
   // Slower version
   $fp = fopen('final.csv', 'w+');
   foreach($data_source as $row) {
       // You may configure fputcsv as usual
       fputcsv($fp, $row);
   }
   fclose($fp);
   ?>
Connex PHP features
-------------------

  + `csv <https://php-dictionary.readthedocs.io/en/latest/dictionary/csv.ini.html>`_


Suggestions
___________

* Use fputcsv() on a memory stream, and flush it on the disk once




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/CsvInLoops                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Performances <ruleset-Performances>`, :ref:`Top10 <ruleset-Top10>`                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


