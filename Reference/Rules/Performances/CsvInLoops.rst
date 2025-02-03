.. _performances-csvinloops:

.. _fputcsv()-in-loops:

fputcsv() In Loops
++++++++++++++++++

.. meta::
	:description:
		fputcsv() In Loops: fputcsv() is slow when called on each row.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: fputcsv() In Loops
	:twitter:description: fputcsv() In Loops: fputcsv() is slow when called on each row
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: fputcsv() In Loops
	:og:type: article
	:og:description: fputcsv() is slow when called on each row
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/fputcsv() In Loops.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/CsvInLoops.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/CsvInLoops.html","name":"fputcsv() In Loops","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"fputcsv() is slow when called on each row","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/fputcsv() In Loops.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>`fputcsv() <https://www.php.net/fputcsv>`_ is slow when called on each row. It actually flushes the data to the disk each time, and that results in a inefficient dump to the disk, each call.

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


