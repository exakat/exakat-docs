.. _performances-doinbase:


.. _do-in-base:

Do In Base
++++++++++

.. meta::
	:description:
		Do In Base: Use SQL expression to compute aggregates in the database.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Do In Base
	:twitter:description: Do In Base: Use SQL expression to compute aggregates in the database
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Do In Base
	:og:type: article
	:og:description: Use SQL expression to compute aggregates in the database
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Do In Base.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/DoInBase.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/DoInBase.html","name":"Do In Base","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Use SQL expression to compute aggregates in the database","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Do In Base.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Use SQL expression to compute aggregates in the database. By doing so, the data don't have to be transfered from the database to PHP, which saves a lot of operations. Such operations are also often faster in the database, because of optimized code.

.. code-block:: php
   
   <?php
   
   // Efficient way
   $res = $db->query('SELECT sum(e) AS sumE FROM table WHERE condition');
   
   // The sum is already done
   $row = $res->fetchArray();
   $c += $row['sumE'];
   
   // Slow way
   $res = $db->query('SELECT e FROM table WHERE condition');
   
   // This aggregates the column e in a slow way
   while($row = $res->fetchArray()) { 
       $c += $row['e'];
   }
   
   ?>
Connex PHP features
-------------------

  + `csv <https://php-dictionary.readthedocs.io/en/latest/dictionary/csv.ini.html>`_


Suggestions
___________

* Rework the query to move the calculations in the database




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/DoInBase                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.8                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


