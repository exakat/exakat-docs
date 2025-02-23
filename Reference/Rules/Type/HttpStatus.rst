.. _type-httpstatus:


.. _http-status-code:

HTTP Status Code
++++++++++++++++

.. meta::
	:description:
		HTTP Status Code: List of all the HTTP status codes mentioned in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: HTTP Status Code
	:twitter:description: HTTP Status Code: List of all the HTTP status codes mentioned in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: HTTP Status Code
	:og:type: article
	:og:description: List of all the HTTP status codes mentioned in the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/HTTP Status Code.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/HttpStatus.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/HttpStatus.html","name":"HTTP Status Code","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"List of all the HTTP status codes mentioned in the code","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/HTTP Status Code.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

List of all the HTTP status codes mentioned in the code.

.. code-block:: php
   
   <?php
   
   http_response_code(418);
   
   header('HTTP/1.1 418 I\'m a teapot');
   
   ?>

See also `List of HTTP status codes <https://en.wikipedia.org/wiki/List_of_HTTP_status_codes>`_.

Connex PHP features
-------------------

  + `Hyper Text Transfer Protocol (HTTP) <https://php-dictionary.readthedocs.io/en/latest/dictionary/http.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/HttpStatus                                                                                                         |
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


