.. _extensions-extstats:

.. _ext-stats:

ext/stats
+++++++++

.. meta::
	:description:
		ext/stats: Statistics extension.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/stats
	:twitter:description: ext/stats: Statistics extension
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/stats
	:og:type: article
	:og:description: Statistics extension
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/stats.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extstats.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extstats.html","name":"ext\/stats","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Statistics extension","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/stats.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Statistics extension.

This extension contains few dozens of functions useful for statistical computations. It is a wrapper around 2 scientific libraries, namely `DCDFLIB <https://people.sc.fsu.edu/~jburkardt/c_src/cdflib/cdflib.html>`_ (Library of C routines for Cumulative Distributions Functions, Inverses, and Other parameters) by B. Brown & J. Lavato and `RANDLIB <http://people.sc.fsu.edu/~jburkardt/f77_src/ranlib/ranlib.html>`_ by Barry Brown, James Lavato & Kathy Russell.

.. code-block:: php
   
   <?php
   
   $x = [ 15, 16, 8, 6, 15, 12, 12, 18, 12, 20, 12, 14, ];
   $y = [ 17.24, 15, 14.91, 4.5, 18, 6.29, 19.23, 18.69, 7.21, 42.06, 7.5, 8,];
   
   sprintf("%2.9f", stats_covariance($a_1, $a_2));
   
   ?>

See also `Statistics <https://www.php.net/manual/en/book.stats.php>`_ and `ext/stats <https://pecl.php.net/package/stats>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extstats                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.5                                                                                                                                                                                  |
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


