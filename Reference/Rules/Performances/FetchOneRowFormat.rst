.. _performances-fetchonerowformat:


.. _fetch-one-row-format:

Fetch One Row Format
++++++++++++++++++++


.. meta::

	:description:

		Fetch One Row Format: When reading results with ext/Sqlite3, it is recommended to explicitly request ``SQLITE3_NUM`` or ``SQLITE3_ASSOC``, while avoiding the default value and ``SQLITE3_BOTH``.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Fetch One Row Format

	:twitter:description: Fetch One Row Format: When reading results with ext/Sqlite3, it is recommended to explicitly request ``SQLITE3_NUM`` or ``SQLITE3_ASSOC``, while avoiding the default value and ``SQLITE3_BOTH``

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Fetch One Row Format

	:og:type: article

	:og:description: When reading results with ext/Sqlite3, it is recommended to explicitly request ``SQLITE3_NUM`` or ``SQLITE3_ASSOC``, while avoiding the default value and ``SQLITE3_BOTH``

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Fetch One Row Format.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/FetchOneRowFormat.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/FetchOneRowFormat.html","name":"Fetch One Row Format","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"When reading results with ext\/Sqlite3, it is recommended to explicitly request ``SQLITE3_NUM`` or ``SQLITE3_ASSOC``, while avoiding the default value and ``SQLITE3_BOTH``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Fetch One Row Format.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When reading results with ext/`Sqlite3 <https://www.php.net/sqlite3>`_, it is recommended to explicitly request ``SQLITE3_NUM`` or ``SQLITE3_ASSOC``, while avoiding the default value and ``SQLITE3_BOTH``.
This is a micro-optimisation. The difference may be visible with 200k rows fetches, and measurable with 10k.

.. code-block:: php
   
   <?php
   
   $res = $database->query($query);
   
   // Fastest version, but less readable
   $row = $res->fetchArray(\SQLITE3_NUM);
   // Almost the fastest version, and more readable
   $row = $res->fetchArray(\SQLITE3_ASSOC);
   
   // Default version. Quite slow
   $row = $res->fetchArray();
   
   // Worse case
   $row = $res->fetchArray(\SQLITE3_BOTH);
   
   ?>
Connex PHP features
-------------------

  + `csv <https://php-dictionary.readthedocs.io/en/latest/dictionary/csv.ini.html>`_


Suggestions
___________

* Specify the result format when reading rows from a Sqlite3 database




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/FetchOneRowFormat                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.6                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


