.. _dump-classinjectioncount:

.. _class-injection-count:

Class Injection Count
+++++++++++++++++++++

.. meta::
	:description:
		Class Injection Count: Counts the number of arguments in the constructor.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Class Injection Count
	:twitter:description: Class Injection Count: Counts the number of arguments in the constructor
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Class Injection Count
	:og:type: article
	:og:description: Counts the number of arguments in the constructor
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Class Injection Count.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/ClassInjectionCount.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/ClassInjectionCount.html","name":"Class Injection Count","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Counts the number of arguments in the constructor","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Class Injection Count.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Counts the number of arguments in the constructor. Variadic arguments are counted as one. The more injections in a constructor, the harder it is to use it. Although, the threshold for difficulty is probably quite high.

.. code-block:: php
   
   <?php
   
   class x {
   	function __constructor(A $a, B, $b) {
   	
   	}
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/ClassInjectionCount                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
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


