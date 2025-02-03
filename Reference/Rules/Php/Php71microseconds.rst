.. _php-php71microseconds:

.. _php-7.1-microseconds:

PHP 7.1 Microseconds
++++++++++++++++++++

.. meta::
	:description:
		PHP 7.1 Microseconds: PHP supports microseconds in ``DateTime`` class and date_create() function.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP 7.1 Microseconds
	:twitter:description: PHP 7.1 Microseconds: PHP supports microseconds in ``DateTime`` class and date_create() function
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP 7.1 Microseconds
	:og:type: article
	:og:description: PHP supports microseconds in ``DateTime`` class and date_create() function
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PHP 7.1 Microseconds.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php71microseconds.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php71microseconds.html","name":"PHP 7.1 Microseconds","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"PHP supports microseconds in ``DateTime`` class and date_create() function","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/PHP 7.1 Microseconds.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>PHP supports microseconds in ``DateTime`` class and `date_create() <https://www.php.net/date_create>`_ function. This was introduced in PHP 7.1.

In previous PHP versions, those dates only used seconds, leading to lazy comparisons : 
This code displays true in PHP 7.0 and older, (unless the code was run too close from the next second). In PHP 7.1, this is always false.

This is also true with ``DateTime`` : 
This evolution impacts mostly exact comparisons (== and ===). Non-equality (!= and !==) will probably be always true, and should be reviewed.

.. code-block:: php
   
   <?php
   
   $now = date_create();
   usleep(10);              // wait for 0.001 ms
   var_dump($now == date_create());
   
   ?>

See also `Backward incompatible changes <https://www.php.net/manual/en/migration71.incompatible.php>`_.

Connex PHP features
-------------------

  + `microtime <https://php-dictionary.readthedocs.io/en/latest/dictionary/microtime.ini.html>`_


Suggestions
___________

* Check direct comparisons of date




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/Php71microseconds                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP71 <ruleset-CompatibilityPHP71>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.9                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                                  |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Major                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                      |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.1                                                                                                                              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                            |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+


