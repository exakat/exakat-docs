.. _structures-basenamesuffix:

.. _use-basename-suffix:

Use Basename Suffix
+++++++++++++++++++

  `basename() <https://www.php.net/basename>`_ is able to remove a file extension when it is provided as argument. The second argument is removed from the name of the file.
Using `basename() <https://www.php.net/basename>`_ instead of `substr() <https://www.php.net/substr>`_ or else, makes the intention clear.

.. code-block:: php
   
   <?php
   
   $path = 'phar:///path/to/file.php';
   
   // Don't forget the . 
   $filename = basename($path, '.php');
   
   // Too much work for this
   $filename = substr(basename($path), 0, -4);
   
   ?>

See also `basename <http://www.php.net/basename>`_.

Connex PHP features
-------------------

  + `basename <https://php-dictionary.readthedocs.io/en/latest/dictionary/basename.ini.html>`_
  + `file-extension <https://php-dictionary.readthedocs.io/en/latest/dictionary/file-extension.ini.html>`_
  + `dirname <https://php-dictionary.readthedocs.io/en/latest/dictionary/dirname.ini.html>`_


Suggestions
___________

* Use basename(), remove more complex code based on substr() or str_replace()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/BasenameSuffix                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-nextcloud-structures-basenamesuffix`, :ref:`case-dolibarr-structures-basenamesuffix`                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


