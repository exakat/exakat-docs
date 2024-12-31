.. _structures-fileusage:

.. _file-usage:

File Usage
++++++++++

.. meta\:\:
	:description:
		File Usage: The application makes usage of files on the system (read, write, delete, etc.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: File Usage
	:twitter:description: File Usage: The application makes usage of files on the system (read, write, delete, etc
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: File Usage
	:og:type: article
	:og:description: The application makes usage of files on the system (read, write, delete, etc
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/FileUsage.html
	:og:locale: en
  The application makes usage of files on the system (read, write, delete, etc.).

Files usage is based on the usage of file functions.

.. code-block:: php
   
   <?php
       $fp = fopen('/tmp/file.txt', 'w+');
       // ....
   ?>

See also `filesystem <http://www.php.net/manual/en/book.filesystem.php>`_.

Connex PHP features
-------------------

  + `file <https://php-dictionary.readthedocs.io/en/latest/dictionary/file.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/FileUsage                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


