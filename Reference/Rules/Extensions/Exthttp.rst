.. _extensions-exthttp:

.. _ext-pecl\_http:

ext/pecl_http
+++++++++++++

.. meta::
	:description:
		ext/pecl_http: Extension HTTP.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/pecl_http
	:twitter:description: ext/pecl_http: Extension HTTP
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/pecl_http
	:og:type: article
	:og:description: Extension HTTP
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/pecl_http.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Exthttp.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Exthttp.html","name":"ext\/pecl_http","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension HTTP","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/pecl_http.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Extension HTTP.

This HTTP extension aims to provide a convenient and powerful set of functionalities for one of PHP major applications.

It eases handling of HTTP URL, headers and messages, provides means for negotiation of a client's preferred content type, language and charset, as well as a convenient way to send any arbitrary data with caching and resuming capabilities.

It provides powerful request functionality with support for parallel requests.

.. code-block:: php
   
   <?php 
   
   $client = new http\Client;
   $client->setSslOptions(array("verifypeer" => true));
   $client->addSslOptions(array("verifyhost" => 2));
   
   $client->enqueue($req = new http\Client\Request("GET", "https://twitter.com/"));
   $client->send();
   $ti = (array) $client->getTransferInfo($req);
   var_dump($ti);
   
   ?>

See also `ext-http <https://github.com/m6w6/ext-http>`_ and `pecl_http <https://pecl.php.net/package/pecl_http>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Exthttp                                                                                                                                                                      |
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


