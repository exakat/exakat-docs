.. _psr-psr7usage:


.. _psr-7-usage:

PSR-7 Usage
+++++++++++

.. meta::
	:description:
		PSR-7 Usage: PSR-7 describes common interfaces for representing HTTP messages as described in `RFC 7230 <https://tools.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PSR-7 Usage
	:twitter:description: PSR-7 Usage: PSR-7 describes common interfaces for representing HTTP messages as described in `RFC 7230 <https://tools
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PSR-7 Usage
	:og:type: article
	:og:description: PSR-7 describes common interfaces for representing HTTP messages as described in `RFC 7230 <https://tools
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PSR-7 Usage.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Psr\/Psr7Usage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Psr\/Psr7Usage.html","name":"PSR-7 Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"PSR-7 describes common interfaces for representing HTTP messages as described in `RFC 7230 <https:\/\/tools","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/PSR-7 Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PSR-7 describes common interfaces for representing HTTP messages as described in `RFC 7230 <https://tools.ietf.org/html/rfc7230>`_ and `RFC 7231 <https://tools.ietf.org/html/rfc7231>`_, and URI for use with HTTP messages as described in `RFC 3986 <https://tools.ietf.org/html/rfc3986>`_. 

It is supported by an set of interfaces, that one may use in the code.

.. code-block:: php
   
   <?php
   
   namespace MyNamespace;
   
   // MyServerRequest implements the PSR-7 ServerRequestInterface.
   // MyServerRequest is more of a black hole than a real Server.
   class MyServerRequest extends  \Psr\Http\Message\ServerRequestInterface  {
       public function getServerParams() {}
       public function getCookieParams() {}
       public function withCookieParams(array $cookies) {}
       public function getQueryParams() {}
       public function withQueryParams(array $query) {}
       public function getUploadedFiles() {}
       public function withUploadedFiles(array $uploadedFiles) {}
       public function getParsedBody() {}
       public function withParsedBody($data) {}
       public function getAttributes() {}
       public function getAttribute($name, $default = null) {}
       public function withAttribute($name, $value) {}
       public function withoutAttribute($name) {}
   }
   
   ?>

See also `PSR-7 : HTTP message interfaces <http://www.php-fig.org/psr/psr-7/>`_.

Connex PHP features
-------------------

  + `PHP Standards Recommendations (PSR) <https://php-dictionary.readthedocs.io/en/latest/dictionary/psr.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Psr/Psr7Usage                                                                                                                                                                           |
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


