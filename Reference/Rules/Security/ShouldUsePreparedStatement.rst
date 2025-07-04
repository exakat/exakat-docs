.. _security-shouldusepreparedstatement:


.. _should-use-prepared-statement:

Should Use Prepared Statement
+++++++++++++++++++++++++++++

.. meta::
	:description:
		Should Use Prepared Statement: Modern databases provides support for prepared statement : it separates the query from the processed data and raise significantly the security.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Should Use Prepared Statement
	:twitter:description: Should Use Prepared Statement: Modern databases provides support for prepared statement : it separates the query from the processed data and raise significantly the security
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Should Use Prepared Statement
	:og:type: article
	:og:description: Modern databases provides support for prepared statement : it separates the query from the processed data and raise significantly the security
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Should Use Prepared Statement.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/ShouldUsePreparedStatement.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/ShouldUsePreparedStatement.html","name":"Should Use Prepared Statement","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Modern databases provides support for prepared statement : it separates the query from the processed data and raise significantly the security","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Should Use Prepared Statement.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Modern databases provides support for prepared statement : it separates the query from the processed data and raise significantly the security. 

Building queries with concatenations is not recommended, though not always avoidable. When possible, use prepared statements.
Same code, without preparation :

.. code-block:: php
   
   <?php
   /* Execute a prepared statement by passing an array of values */
   
   $sql = 'SELECT name, colour, calories
       FROM fruit
       WHERE calories < :calories AND colour = :colour';
   $sth = $conn->prepare($sql, array(PDO::ATTR_CURSOR => PDO::CURSOR_FWDONLY));
   $sth->execute(array(':calories' => 150, ':colour' => 'red'));
   $red = $sth->fetchAll();
   ?>

+-------------+--------------------+------+----------------------------+
| Name        | Default            | Type | Description                |
+-------------+--------------------+------+----------------------------+
| queryMethod | query_methods.json | data | Methods that call a query. |
+-------------+--------------------+------+----------------------------+



See also `Prepared Statements <https://www.php.net/manual/en/mysqli.quickstart.prepared-statements.php>`_, `PHP MySQLi Prepared Statements Tutorial to Prevent SQL Injection <https://websitebeaver.com/prepared-statements-in-php-mysqli-to-prevent-sql-injection>`_ and `The Best Way to Perform MYSQLI Prepared Statements in PHP <https://developer.hyvor.com/php/prepared-statements>`_.


Suggestions
___________

* Use an ORM
* Use an Active Record library
* Change the query to hard code it and make it not injectable




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/ShouldUsePreparedStatement                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolibarr-security-shouldusepreparedstatement`                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


