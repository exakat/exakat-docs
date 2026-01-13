.. _structures-fileputcontentsdatatype:

.. _file\_put\_contents-using-array-argument:

File_Put_Contents Using Array Argument
++++++++++++++++++++++++++++++++++++++

  `file_put_contents() <https://www.php.net/file_put_contents>`_ accepts a second argument as an array, and stores it in the file with an implicit implode. This is a documented behavior, though it is rarely used.

.. code-block:: php
   
   <?php
   
   file_put_contents('/tmp/file.txt', [1, 2, 3, 4]);
   
   print file_get_contents('/tmp/file.txt'); 
   // displays 1234
   
   ?>

See also `file_put_contents() <https://www.php.net/file_put_contents>`_.

Connex PHP features
-------------------

  + `silent <https://php-dictionary.readthedocs.io/en/latest/dictionary/silent.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/FilePutContentsDataType                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.5                                                                                                                   |
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


