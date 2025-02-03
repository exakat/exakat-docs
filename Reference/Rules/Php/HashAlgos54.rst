.. _php-hashalgos54:

.. _hash-algorithms-incompatible-with-php-5.4-5.5:

Hash Algorithms Incompatible With PHP 5.4/5.5
+++++++++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Hash Algorithms Incompatible With PHP 5.4/5.5: List of hash algorithms incompatible with PHP 5.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Hash Algorithms Incompatible With PHP 5.4/5.5
	:twitter:description: Hash Algorithms Incompatible With PHP 5.4/5.5: List of hash algorithms incompatible with PHP 5
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Hash Algorithms Incompatible With PHP 5.4/5.5
	:og:type: article
	:og:description: List of hash algorithms incompatible with PHP 5
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Hash Algorithms Incompatible With PHP 5.4/5.5.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/HashAlgos54.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/HashAlgos54.html","name":"Hash Algorithms Incompatible With PHP 5.4\/5.5","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"List of hash algorithms incompatible with PHP 5","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Hash Algorithms Incompatible With PHP 5.4\/5.5.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>List of hash algorithms incompatible with PHP 5.4 and 5.5.

.. code-block:: php
   
   <?php
   
   // Compatible only with 5.4 and more recent
   echo hash('fnv132', 'The quick brown fox jumped over the lazy dog.');
   
   // Always compatible
   echo hash('ripemd320', 'The quick brown fox jumped over the lazy dog.');
   
   ?>

See also `hash_algos <https://www.php.net/hash_algos>`_.


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/HashAlgos54                                                                                                                                                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>`, :ref:`CompatibilityPHP71 <ruleset-CompatibilityPHP71>`, :ref:`CompatibilityPHP72 <ruleset-CompatibilityPHP72>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.4 and older                                                                                                                                                                                                                                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


