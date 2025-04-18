.. _type-httpheader:


.. _http-headers:

Http Headers
++++++++++++

.. meta::
	:description:
		Http Headers: List of HTTP headers use in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Http Headers
	:twitter:description: Http Headers: List of HTTP headers use in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Http Headers
	:og:type: article
	:og:description: List of HTTP headers use in the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Http Headers.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/HttpHeader.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/HttpHeader.html","name":"Http Headers","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"List of HTTP headers use in the code","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Http Headers.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

List of HTTP headers use in the code. 
Those headers are mostly used with `header() <https://www.php.net/header>`_ function to send to browser.

.. code-block:: php
   
   <?php
   
   header('Location: http://www.example.com/');
   
   // Parseable headers are also reported
   header('Location: http://www.example.com/');
   
   // UnParseable headers are not reported
   header('GarbagexxxxXXXXxxxGarbagexxxxXXXXxxx');
   header($header);
   
   ?>

See also `List of HTTP header fields <https://en.wikipedia.org/wiki/List_of_HTTP_header_fields>`_.

Connex PHP features
-------------------

  + `Hyper Text Transfer Protocol (HTTP) <https://php-dictionary.readthedocs.io/en/latest/dictionary/http.ini.html>`_
  + `HTTP Headers <https://php-dictionary.readthedocs.io/en/latest/dictionary/http-header.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/HttpHeader                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Inventory <ruleset-Inventory>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


