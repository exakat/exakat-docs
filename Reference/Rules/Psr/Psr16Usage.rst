.. _psr-psr16usage:


.. _psr-16-usage:

PSR-16 Usage
++++++++++++


.. meta::

	:description:

		PSR-16 Usage: PSR-16 describes a simple yet extensible interface for a cache item and a cache driver.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: PSR-16 Usage

	:twitter:description: PSR-16 Usage: PSR-16 describes a simple yet extensible interface for a cache item and a cache driver

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: PSR-16 Usage

	:og:type: article

	:og:description: PSR-16 describes a simple yet extensible interface for a cache item and a cache driver

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PSR-16 Usage.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Psr\/Psr16Usage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Psr\/Psr16Usage.html","name":"PSR-16 Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"PSR-16 describes a simple yet extensible interface for a cache item and a cache driver","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/PSR-16 Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PSR-16 describes a simple yet extensible interface for a cache item and a cache driver. It is supported by an set of interfaces, that one may use in the code.

.. code-block:: php
   
   <?php
   
   namespace My\SimpleCache;
   
   // MyCache implements the PSR-16 Simple cache.
   // MyCache is more of a black hole than a real cache.
   class MyCache implements Psr\SimpleCache\CacheInterface {
       public function get($key, $default = null) {}
       public function set($key, $value, $ttl = null) {}
       public function delete($key) {}
       public function clear() {}
       public function getMultiple($keys, $default = null) {}
       public function setMultiple($values, $ttl = null) {}
       public function deleteMultiple($keys) {}
       public function has($key) {}
   }
   
   ?>

See also `PSR-16 : Common Interface for Caching Libraries <http://www.php-fig.org/psr/psr-16/>`_.

Connex PHP features
-------------------

  + `psr <https://php-dictionary.readthedocs.io/en/latest/dictionary/psr.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Psr/Psr16Usage                                                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.6                                                                                                                                                                                  |
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


