.. _php-hashalgos:


.. _hash-algorithms:

Hash Algorithms
+++++++++++++++

.. meta::
	:description:
		Hash Algorithms: There is a long but limited list of hashing algorithm available to PHP.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Hash Algorithms
	:twitter:description: Hash Algorithms: There is a long but limited list of hashing algorithm available to PHP
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Hash Algorithms
	:og:type: article
	:og:description: There is a long but limited list of hashing algorithm available to PHP
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Hash Algorithms.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/HashAlgos.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/HashAlgos.html","name":"Hash Algorithms","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"There is a long but limited list of hashing algorithm available to PHP","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Hash Algorithms.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

There is a long but limited list of hashing algorithm available to PHP. The one found doesn't seem to be existing.

.. code-block:: php
   
   <?php
   
   // This hash has existed in PHP. Check with hash_algos() if it is available on your system. 
   echo hash('ripmed160', 'The quick brown fox jumped over the lazy dog.');
   
   // This hash doesn't exist
   echo hash('ripemd160', 'The quick brown fox jumped over the lazy dog.');
   
   ?>

See also `hash_algos <https://www.php.net/hash_algos>`_.

Connex PHP features
-------------------

  + `Hash <https://php-dictionary.readthedocs.io/en/latest/dictionary/hash.ini.html>`_


Suggestions
___________

* Use a hash algorithm that is available on several PHP versions
* Fix the name of the hash algorithm




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/HashAlgos                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


