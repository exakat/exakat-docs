.. _extensions-extmemcache:


.. _ext-memcache:

ext/memcache
++++++++++++

.. meta::
	:description:
		ext/memcache: Extension Memcache.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/memcache
	:twitter:description: ext/memcache: Extension Memcache
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/memcache
	:og:type: article
	:og:description: Extension Memcache
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/memcache.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extmemcache.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extmemcache.html","name":"ext\/memcache","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension Memcache","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/memcache.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension Memcache.

Memcache module provides handy procedural and object oriented interface to memcached, highly effective caching daemon, which was especially designed to decrease database load in dynamic web applications.

.. code-block:: php
   
   <?php
   
   $memcache = new Memcache;
   $memcache->connect('localhost', 11211) or die ('Could not connect');
   
   $version = $memcache->getVersion();
   echo 'Server\'s version: '.$version.'<br/>';
   
   $tmp_object = new stdClass;
   $tmp_object->str_attr = 'test';
   $tmp_object->int_attr = 123;
   
   $memcache->set('key', $tmp_object, false, 10) or die ('Failed to save data at the server');
   echo 'Store data in the cache (data will expire in 10 seconds)<br/>';
   
   $get_result = $memcache->get('key');
   echo 'Data from the cache:<br/>';
   
   var_dump($get_result);
   
   ?>

See also `Memcache on PHP <http://www.php.net/manual/en/book.memcache.php>`_ and `memcache on github <https://github.com/websupport-sk/pecl-memcache>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extmemcache                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
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


