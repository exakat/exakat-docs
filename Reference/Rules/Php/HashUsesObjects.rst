.. _php-hashusesobjects:


.. _hash-will-use-objects:

Hash Will Use Objects
+++++++++++++++++++++

.. meta::
	:description:
		Hash Will Use Objects: The `ext/hash extension <http://www.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Hash Will Use Objects
	:twitter:description: Hash Will Use Objects: The `ext/hash extension <http://www
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Hash Will Use Objects
	:og:type: article
	:og:description: The `ext/hash extension <http://www
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Hash Will Use Objects.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/HashUsesObjects.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/HashUsesObjects.html","name":"Hash Will Use Objects","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The `ext\/hash extension <http:\/\/www","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Hash Will Use Objects.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The `ext/hash extension <http://www.php.net/manual/en/book.hash.php>`_ used resources, and is being upgraded to use resources.

.. code-block:: php
   
   <?php
   
   // Post 7.2 code 
       $hash = hash_init('sha256');
       if (!is_object($hash)) {
           trigger_error('error');
       }
       hash_update($hash, $message);
   
   // Pre-7.2 code
       $hash = hash_init('md5');
       if (!is_resource($hash)) {
           trigger_error('error');
       }
       hash_update($hash, $message);
   
   ?>

See also `Move ext/hash from resources to objects <https://www.php.net/manual/en/migration72.incompatible.php#migration72.incompatible.hash-ext-to-objects>`_.

Connex PHP features
-------------------

  + `Hash <https://php-dictionary.readthedocs.io/en/latest/dictionary/hash.ini.html>`_
  + `Object <https://php-dictionary.readthedocs.io/en/latest/dictionary/object.ini.html>`_


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/HashUsesObjects                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP72 <ruleset-CompatibilityPHP72>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


