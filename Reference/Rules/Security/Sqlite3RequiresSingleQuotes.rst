.. _security-sqlite3requiressinglequotes:


.. _sqlite3-requires-single-quotes:

Sqlite3 Requires Single Quotes
++++++++++++++++++++++++++++++

.. meta::
	:description:
		Sqlite3 Requires Single Quotes: The escapeString() method from ``SQLite3`` doesn't escape ``"``, but only ``'``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Sqlite3 Requires Single Quotes
	:twitter:description: Sqlite3 Requires Single Quotes: The escapeString() method from ``SQLite3`` doesn't escape ``"``, but only ``'``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Sqlite3 Requires Single Quotes
	:og:type: article
	:og:description: The escapeString() method from ``SQLite3`` doesn't escape ``"``, but only ``'``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Sqlite3 Requires Single Quotes.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/Sqlite3RequiresSingleQuotes.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/Sqlite3RequiresSingleQuotes.html","name":"Sqlite3 Requires Single Quotes","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The escapeString() method from ``SQLite3`` doesn't escape ``\"``, but only ``'``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Sqlite3 Requires Single Quotes.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The escapeString() method from ``SQLite3`` doesn't escape ``"``, but only ``'``. 
To properly handle quotes and ``NUL`` characters, use bindParam() instead.

Quote from the PHP manual comments : ``The reason this function doesn't escape double quotes is because double quotes are used with names (the equivalent of backticks in MySQL), as in table or column names, while single quotes are used for values.``

.. code-block:: php
   
   <?php
   
   // OK. escapeString is OK with '
   $query = "SELECT * FROM table WHERE col = '".$sqlite->escapeString($x)."'";
   
   // This is vulnerable to " in $x
   $query = 'SELECT * FROM table WHERE col = "'.$sqlite->escapeString($x).'"';
   
   ?>

See also `SQLite3::escapeString <https://www.php.net/manual/en/sqlite3.escapestring.php>`_.

Connex PHP features
-------------------

  + `Sqlite3 <https://php-dictionary.readthedocs.io/en/latest/dictionary/sqlite3.ini.html>`_


Suggestions
___________

* Use prepared statements whenever possible
* Switch the query to use single quote




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/Sqlite3RequiresSingleQuotes                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.10                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


