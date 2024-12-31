.. _extensions-extfam:

.. _ext-fam:

ext/fam
+++++++

.. meta\:\:
	:description:
		ext/fam: File Alteration Monitor extension.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/fam
	:twitter:description: ext/fam: File Alteration Monitor extension
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/fam
	:og:type: article
	:og:description: File Alteration Monitor extension
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extfam.html
	:og:locale: en
  File Alteration Monitor extension.

`FAM <http://oss.sgi.com/projects/fam/>`_ monitors files and directories, notifying interested applications of changes.

ext/FAM is not available for Windows

.. code-block:: php
   
   <?php
   
   $fam = fam_open('myApplication');
   fam_monitor_directory($fam, '/tmp');
   fam_close($fam);
   
   ?>

See also `File Alteration Monitor <https://www.php.net/manual/en/book.fam.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extfam                                                                                                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.8                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


