.. _php-utf8encodedeprecated:


.. _utf8-encode-and-decode-are-deprecated:

Utf8 Encode And Decode Are Deprecated
+++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Utf8 Encode And Decode Are Deprecated: utf8_encode() and utf8_decode() are deprecated in PHP 8.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Utf8 Encode And Decode Are Deprecated
	:twitter:description: Utf8 Encode And Decode Are Deprecated: utf8_encode() and utf8_decode() are deprecated in PHP 8
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Utf8 Encode And Decode Are Deprecated
	:og:type: article
	:og:description: utf8_encode() and utf8_decode() are deprecated in PHP 8
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Utf8 Encode And Decode Are Deprecated.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Utf8EncodeDeprecated.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Utf8EncodeDeprecated.html","name":"Utf8 Encode And Decode Are Deprecated","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"utf8_encode() and utf8_decode() are deprecated in PHP 8","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Utf8 Encode And Decode Are Deprecated.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`utf8_encode() <https://www.php.net/utf8_encode>`_ and `utf8_decode() <https://www.php.net/utf8_decode>`_ are deprecated in PHP 8.0. They are planned removal in PHP 9.0.

See also `PHP RFC: Deprecate and Remove utf8_encode and utf8_decode <https://wiki.php.net/rfc/remove_utf8_decode_and_utf8_encode>`_.


Suggestions
___________

* Use mbstring functions : mb_convert_encoding($latin1, 'UTF-8', 'ISO-8859-1')
* Use iconv functions : mb_convert_encoding($latin1, 'UTF-8', 'ISO-8859-1')
* Use intl functions : iconv('ISO-8859-1', 'UTF-8', $latin1)




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Utf8EncodeDeprecated                                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP82 <ruleset-CompatibilityPHP82>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.5                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.2 and more recent                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


