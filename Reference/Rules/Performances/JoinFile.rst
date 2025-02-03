.. _performances-joinfile:


.. _joining-file():

Joining file()
++++++++++++++


.. meta::

	:description:

		Joining file(): Use file() to read lines separately.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Joining file()

	:twitter:description: Joining file(): Use file() to read lines separately

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Joining file()

	:og:type: article

	:og:description: Use file() to read lines separately

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Joining file().html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/JoinFile.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/JoinFile.html","name":"Joining file()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Use file() to read lines separately","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Joining file().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Use `file() <https://www.php.net/file>`_ to read lines separately. 

Applying ``join('', )`` or ``implode('', )`` to the `result <https://www.php.net/result>`_ of `file() <https://www.php.net/file>`_ provides the same results than using `file_get_contents() <https://www.php.net/file_get_contents>`_, but at a higher cost of memory and processing.

If the delimiter is not ``''``, then ``implode()`` and ``file()`` are a better solution than ``file_get_contents()`` and ``str_replace()`` or ``nl2br()``.

Always use ``file_get_contents()`` to get the content of a file as a string. Consider using `readfile() <https://www.php.net/readfile>`_ to echo the content directly to the output.

This analysis also checks for the reverse feature: loading a file with ``file_get_contents()`` and splitting it into rows with ``explode()`` or an alternative. Such association should be replaced by a single call to ``file()``, with may be the ``FILE_IGNORE_NEW_LINES``.


.. code-block:: php
   
   <?php
   
   // memory intensive
   $content = file_get_contents('path/to/file.txt');
   
   // memory and CPU intensive
   $content = join('', file('path/to/file.txt'));
   
   // Consider reading the data line by line and processing it along the way, 
   // to save memory 
   $fp = fopen('path/to/file.txt', 'r');
   while($line = fget($fp)) {
       // process a line
   }
   fclose($fp);
   
   // Reverse feature 
   $file = file_get_contents('/path/to/file.txt');
   $rows = explode(PHP_EOL, $file);
   
   ?>

See also `file_get_contents <https://www.php.net/file_get_contents>`_, `file <https://www.php.net/file>`_ and `explode <https://www.php.net/explode>`_.

Connex PHP features
-------------------

  + `csv <https://php-dictionary.readthedocs.io/en/latest/dictionary/csv.ini.html>`_


Suggestions
___________

* Use file_get_contents() instead of implode(file()) to read the whole file at once.
* Use readfile() to echo the content to standard output ``stdout`` at once.
* Use fopen() to read the lines one by one, generator style.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/JoinFile                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Performances <ruleset-Performances>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-performances-joinfile`, :ref:`case-spip-performances-joinfile`                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


