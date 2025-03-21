.. _extensions-extpgsql:


.. _ext-pgsql:

ext/pgsql
+++++++++

.. meta::
	:description:
		ext/pgsql: Extension PostGreSQL.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/pgsql
	:twitter:description: ext/pgsql: Extension PostGreSQL
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/pgsql
	:og:type: article
	:og:description: Extension PostGreSQL
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/pgsql.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extpgsql.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extpgsql.html","name":"ext\/pgsql","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension PostGreSQL","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/pgsql.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension PostGreSQL.

PostgreSQL is an open source descendant of this original Berkeley code.  It provides SQL92/SQL99 language support, transactions, referential integrity, stored procedures and type extensibility.

.. code-block:: php
   
   <?php
   // Connect to a database named 'mary'
   $dbconn = pg_connect('dbname=mary');
   
   // Prepare a query for execution
   $result = pg_prepare($dbconn, 'my_query', 'SELECT * FROM shops WHERE name = $1');
   
   // Execute the prepared query.  Note that it is not necessary to escape
   // the string 'Joe's Widgets' in any way
   $result = pg_execute($dbconn, 'my_query', array('Joe\'s Widgets'));
   
   // Execute the same prepared query, this time with a different parameter
   $result = pg_execute($dbconn, 'my_query', array('Clothes Clothes Clothes'));
   
   ?>

See also `PostgreSQL <https://www.php.net/manual/en/book.pgsql.php>`_ and `PostgreSQL: The world's most advanced open source database <https://www.postgresql.org/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extpgsql                                                                                                                                                                     |
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


