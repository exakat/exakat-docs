.. _performances-joinfile:

.. _joining-file():

Joining file()
++++++++++++++

  Use `file() <https://www.php.net/file>`_ to read lines separately. 

Applying ``join('', )`` or ``implode('', )`` to the `result <https://www.php.net/result>`_ of `file() <https://www.php.net/file>`_ provides the same results than using `file_get_contents() <https://www.php.net/file_get_contents>`_, but at a higher cost of memory and processing.

If the delimiter is not ``''``, then ``implode()`` and ``file()`` are a better solution than ``file_get_contents()`` and ``str_replace()`` or ``nl2br()``.

Always use ``file_get_contents()`` to get the content of a file as a string. Consider using `readfile() <https://www.php.net/readfile>`_ to echo the content directly to the output.

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
   
   ?>

See also `file_get_contents <https://www.php.net/file_get_contents>`_ and `file <https://www.php.net/file>`_.


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
| Features     | csv                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-performances-joinfile`, :ref:`case-spip-performances-joinfile`                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


