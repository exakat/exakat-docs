.. _dump-dereferencinglevels:


.. _dereferencing-levels:

Dereferencing Levels
++++++++++++++++++++

.. meta::
	:description:
		Dereferencing Levels: This is the counts of level of dereferencing.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Dereferencing Levels
	:twitter:description: Dereferencing Levels: This is the counts of level of dereferencing
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Dereferencing Levels
	:og:type: article
	:og:description: This is the counts of level of dereferencing
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Dereferencing Levels.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/DereferencingLevels.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/DereferencingLevels.html","name":"Dereferencing Levels","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This is the counts of level of dereferencing","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Dereferencing Levels.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This is the counts of level of dereferencing. 

Every time a `->` object operator or `?->` `null <https://www.php.net/`null <https://www.php.net/null>`_>`_-safe object operator are used, this count as one level of dereferencing. 

Fluent interfaces tends to have very high levels of deferencing.

.. code-block:: php
   
   <?php
   
   // one level of dereferencing 
   $a->b;
   $c->d();
   
   // four levels of dereferencing
   $a->b->c()->d->e();
   
   // also four levels of dereferencing
   $a->b?->c()->d->e();
   
   ?>
Connex PHP features
-------------------

  + `Dereferencing <https://php-dictionary.readthedocs.io/en/latest/dictionary/dereferencing.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/DereferencingLevels                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.6                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


