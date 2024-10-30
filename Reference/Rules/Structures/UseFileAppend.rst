.. _structures-usefileappend:

.. _use-file-append:

Use File Append
+++++++++++++++

  When appending data to a file, one may also use the `file_put_contents() <https://www.php.net/file_put_contents>`_ function with the ``FILE_APPEND`` option. 

Using `file_put_contents() <https://www.php.net/file_put_contents>`_ also keeps the file open as little as possible, unlike keeping the resource open in PHP, between usages.

.. code-block:: php
   
   <?php
   
   // appends the text to the end of the end of the file
   file_put_contents($file, $text, FILE_APPEND);
   
   // appends the text to the end of the end of the file
   $fp = fopen($file, 'a');
   fwrite($fp, $text);
   
   ?>
Connex PHP features
-------------------

  + `file <https://php-dictionary.readthedocs.io/en/latest/dictionary/file.ini.html>`_


Suggestions
___________

* Use file_put_contents()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UseFileAppend                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.5                                                                                                                   |
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


