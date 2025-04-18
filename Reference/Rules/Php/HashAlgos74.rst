.. _php-hashalgos74:


.. _hash-algorithms-incompatible-with-php-7.4-:

Hash Algorithms Incompatible With PHP 7.4-
++++++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Hash Algorithms Incompatible With PHP 7.4-: List of hash algorithms incompatible with PHP 7.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Hash Algorithms Incompatible With PHP 7.4-
	:twitter:description: Hash Algorithms Incompatible With PHP 7.4-: List of hash algorithms incompatible with PHP 7
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Hash Algorithms Incompatible With PHP 7.4-
	:og:type: article
	:og:description: List of hash algorithms incompatible with PHP 7
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Hash Algorithms Incompatible With PHP 7.4-.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/HashAlgos74.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/HashAlgos74.html","name":"Hash Algorithms Incompatible With PHP 7.4-","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"List of hash algorithms incompatible with PHP 7","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Hash Algorithms Incompatible With PHP 7.4-.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

List of hash algorithms incompatible with PHP 7.3 and older recent. At the moment of writing, this is compatible up to 7.4s. 

The hash algorithms were introduced in PHP 7.4s.

.. code-block:: php
   
   <?php
   
   // Compatible only with 7.1 and more recent
   echo hash('crc32cs', 'The quick brown fox jumped over the lazy dog.');
   
   // Always compatible
   echo hash('ripemd320', 'The quick brown fox jumped over the lazy dog.');
   
   ?>

See also `hash_algos <https://www.php.net/hash_algos>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/HashAlgos74                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and older                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


