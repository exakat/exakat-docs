.. _extensions-extibase:

.. _ext-ibase:

ext/ibase
+++++++++

.. meta::
	:description:
		ext/ibase: Extensions ``Interbase`` and ``Firebird``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/ibase
	:twitter:description: ext/ibase: Extensions ``Interbase`` and ``Firebird``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/ibase
	:og:type: article
	:og:description: Extensions ``Interbase`` and ``Firebird``
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extibase.html
	:og:locale: en
Extensions ``Interbase`` and ``Firebird``.

``Firebird`` is a relational database offering many ISO SQL-2003 features that runs on Linux, Windows, and a variety of Unix platforms.

.. code-block:: php
   
   <?php
   
   $host = 'localhost:/path/to/your.gdb';
   
   $dbh = ibase_connect($host, $username, $password);
   $stmt = 'SELECT * FROM tblname';
   
   $sth = ibase_query($dbh, $stmt) or die(ibase_errmsg());
   
   ?>

See also `Firebase / Interbase <https://www.php.net/manual/en/book.ibase.php>`_ and `Firebird <http://www.firebirdsql.org/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extibase                                                                                                                                                                     |
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
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


