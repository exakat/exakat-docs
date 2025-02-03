.. _php-yieldusage:

.. _yield-usage:

Yield Usage
+++++++++++

.. meta::
	:description:
		Yield Usage: Usage of generators, with yield keyword.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Yield Usage
	:twitter:description: Yield Usage: Usage of generators, with yield keyword
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Yield Usage
	:og:type: article
	:og:description: Usage of generators, with yield keyword
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Yield Usage.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/YieldUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/YieldUsage.html","name":"Yield Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Usage of generators, with yield keyword","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Yield Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Usage of generators, with yield keyword.

Yield was introduced in PHP 5.5, and is backward incompatible.

.. code-block:: php
   
   <?php
   
   function prime() {
       $primes = [2, 3, 5, 7, 11, 13, 17, 19];
       foreach($primes as $prime) {
           yield $prime;
       }
   }
   
   ?>

See also `Generator Syntax <https://www.php.net/manual/en/language.generators.syntax.php>`_, `Deal with Memory Gently using "Yield" in PHP <https://medium.com/tech-tajawal/use-memory-gently-with-yield-in-php-7e62e2480b8d>`_ and `Understanding PHP Generators <https://scotch.io/tutorials/understanding-php-generators>`_.

Connex PHP features
-------------------

  + `yield <https://php-dictionary.readthedocs.io/en/latest/dictionary/yield.ini.html>`_
  + `yield-from <https://php-dictionary.readthedocs.io/en/latest/dictionary/yield-from.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/YieldUsage                                                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.5 and more recent                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


