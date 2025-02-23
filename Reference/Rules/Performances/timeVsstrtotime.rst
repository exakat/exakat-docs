.. _performances-timevsstrtotime:


.. _time()-vs-strtotime():

time() Vs strtotime()
+++++++++++++++++++++

.. meta::
	:description:
		time() Vs strtotime(): time() is actually faster than strtotime() with 'now' key string.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: time() Vs strtotime()
	:twitter:description: time() Vs strtotime(): time() is actually faster than strtotime() with 'now' key string
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: time() Vs strtotime()
	:og:type: article
	:og:description: time() is actually faster than strtotime() with 'now' key string
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/time() Vs strtotime().html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/timeVsstrtotime.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/timeVsstrtotime.html","name":"time() Vs strtotime()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"time() is actually faster than strtotime() with 'now' key string","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/time() Vs strtotime().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`time() <https://www.php.net/time>`_ is actually faster than `strtotime() <https://www.php.net/strtotime>`_ with 'now' key string.
This is a micro-optimisation. Relative gain is real, but small unless the function is used many times.

.. code-block:: php
   
   <?php
   
   // Faster version
   $a = time();
   
   // Slower version
   $b = strtotime('now');
   
   ?>
Connex PHP features
-------------------

  + `declare() <https://php-dictionary.readthedocs.io/en/latest/dictionary/declare.ini.html>`_


Suggestions
___________

* Replace strtotime() with time(). Do not change strtotime() with other value than 'now'.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/timeVsstrtotime                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.7                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-woocommerce-performances-timevsstrtotime`                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


