.. _extensions-extrar:

.. _ext-rar:

ext/rar
+++++++

.. meta::
	:description:
		ext/rar: Extension RAR.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/rar
	:twitter:description: ext/rar: Extension RAR
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/rar
	:og:type: article
	:og:description: Extension RAR
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/rar.html
	:og:locale: en
Extension RAR. 

Rar is a powerful and effective archiver created by Eugene Roshal. This extension gives you possibility to read Rar archives but doesn't support writing Rar archives, because this is not supported by the UnRar library and is directly prohibited by its license.

.. code-block:: php
   
   <?php
   
   $arch = RarArchive::open(example.rar);
   if ($arch === FALSE)
       die(Cannot open example.rar);
   
   $entries = $arch->getEntries();
   if ($entries === FALSE)
       die(Cannot retrieve entries);
   
   
   ?>

See also `Rar archiving <https://www.php.net/manual/en/book.rar.php>`_ and `rarlabs <http://www.rarlabs.com/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extrar                                                                                                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.7                                                                                                                                                                                   |
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


