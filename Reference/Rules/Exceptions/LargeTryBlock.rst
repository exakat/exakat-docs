.. _exceptions-largetryblock:

.. _large-try-block:

Large Try Block
+++++++++++++++

.. meta::
	:description:
		Large Try Block: Try block should enclosing only the expression that may emit an exception.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Large Try Block
	:twitter:description: Large Try Block: Try block should enclosing only the expression that may emit an exception
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Large Try Block
	:og:type: article
	:og:description: Try block should enclosing only the expression that may emit an exception
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Large Try Block.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/LargeTryBlock.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/LargeTryBlock.html","name":"Large Try Block","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"Try block should enclosing only the expression that may emit an exception","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Large Try Block.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Try block should enclosing only the expression that may emit an `exception <https://www.php.net/exception>`_. 

When writing large blocks of code in a try, it becomes difficult to understand where the expression is coming from. Large blocks may also lead to catch multiples exceptions, with a long list of catch clause. 

In particular, the catch clause resumes the execution without knowing where the try was interrupted : there are no indication of achievement, even partial. In fact, catching an `exception <https://www.php.net/exception>`_ signals a very dirty situation.
This analysis reports try blocks that are 5 lines or more. This threshold may be configured with the directive ``tryBlockMaxSize``. Catch clause, and finally are not considered here.

.. code-block:: php
   
   <?php
   
   // try is one expression only
   try {
       $database->query($query);
   } catch (DatabaseException $e) {
       // process exception
   }
   
   // Too many expressions around the one that may actually emit the exception
   try {
       $SQL = build_query($arguments);
       $database = new Database($dsn);
       $database->setOption($options);
       $statement = $database->prepareQuery($SQL);
       $result = $statement->query($query);
   } catch (DatabaseException $e) {
       // process exception
   }
   
   ?>

+-----------------+---------+---------+-------------------------------------------------+
| Name            | Default | Type    | Description                                     |
+-----------------+---------+---------+-------------------------------------------------+
| tryBlockMaxSize | 5       | integer | Maximal number of expressions in the try block. |
+-----------------+---------+---------+-------------------------------------------------+



See also `Exceptions <https://www.php.net/manual/en/language.exceptions.php>`_.

Connex PHP features
-------------------

  + `try-catch <https://php-dictionary.readthedocs.io/en/latest/dictionary/try-catch.ini.html>`_


Suggestions
___________

* Reduce the amount of code in the block, by moving it before and after




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/LargeTryBlock                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


