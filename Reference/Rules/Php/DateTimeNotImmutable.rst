.. _php-datetimenotimmutable:

.. _datetimeimmutable-is-not-immutable:

DateTimeImmutable Is Not Immutable
++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		DateTimeImmutable Is Not Immutable: ``DateTimeImmutable`` is not really immutable because its internal state can be modified after instantiation.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: DateTimeImmutable Is Not Immutable
	:twitter:description: DateTimeImmutable Is Not Immutable: ``DateTimeImmutable`` is not really immutable because its internal state can be modified after instantiation
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: DateTimeImmutable Is Not Immutable
	:og:type: article
	:og:description: ``DateTimeImmutable`` is not really immutable because its internal state can be modified after instantiation
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/DateTimeImmutable Is Not Immutable.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/DateTimeNotImmutable.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/DateTimeNotImmutable.html","name":"DateTimeImmutable Is Not Immutable","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"``DateTimeImmutable`` is not really immutable because its internal state can be modified after instantiation","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/DateTimeImmutable Is Not Immutable.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>``DateTimeImmutable`` is not really immutable because its internal state can be modified after instantiation.
Inspired by the article from ``Matthias Noback``.

.. code-block:: php
   
   <?php
   
   $dt = new DateTimeImmutable('now');
   echo $dt->getTimestamp() . "\n";
   
   $dt->__construct('tomorrow');
   echo $dt->getTimestamp() . "\n";
   
   ?>

See also `Effective immutability with PHPStan <https://matthiasnoback.nl/2022/07/effective-immutability-with-phpstan/>`_.


Suggestions
___________

* Remove the call to the constructor after instantation of a DateTimeImmutable object




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/DateTimeNotImmutable                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


