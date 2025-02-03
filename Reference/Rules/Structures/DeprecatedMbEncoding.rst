.. _structures-deprecatedmbencoding:


.. _deprecated-mb\_string-encodings:

Deprecated Mb_string Encodings
++++++++++++++++++++++++++++++


.. meta::

	:description:

		Deprecated Mb_string Encodings: Some encodings, available in the mb_string extensions, are deprecated.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Deprecated Mb_string Encodings

	:twitter:description: Deprecated Mb_string Encodings: Some encodings, available in the mb_string extensions, are deprecated

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Deprecated Mb_string Encodings

	:og:type: article

	:og:description: Some encodings, available in the mb_string extensions, are deprecated

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Deprecated Mb_string Encodings.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/DeprecatedMbEncoding.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/DeprecatedMbEncoding.html","name":"Deprecated Mb_string Encodings","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 16 Jan 2025 17:40:16 +0000","dateModified":"Thu, 16 Jan 2025 17:40:16 +0000","description":"Some encodings, available in the mb_string extensions, are deprecated","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Deprecated Mb_string Encodings.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Some encodings, available in the mb_string extensions, are deprecated. Starting with PHP 8.2, the following encodings emits a warning: 

+ BASE64
+ UUENCODE
+ HTML-ENTITIES
+ html
+ Quoted-Printable
+ qprint

This applies to the `mb_detect_encoding() <https://www.php.net/mb_detect_encoding>`_ and `mb_convert_encoding() <https://www.php.net/mb_convert_encoding>`_ functions.

.. code-block:: php
   
   <?php
   
   // recommended version
   $base64Encoded = base64_encode('test'));
   
   // Deprecated version
   mb_convert_encoding('test', 'base64'));
   
   ?>

See also `PHP 8.2: Mbstring: Base64, Uuencode, QPrint, and HTML Entity encodings are deprecated <https://php.watch/versions/8.2/mbstring-qprint-base64-uuencode-html-entities-deprecated>`_.

Related PHP errors 
-------------------

  + `mb_convert_encoding(): Handling Base64 via mbstring is deprecated; use base64_encode/base64_decode instead <https://php-errors.readthedocs.io/en/latest/messages/handling-base64-via-mbstring-is-deprecated%3B-use-base64_encode-base64_decode-instead.html>`_
  + `Handling HTML entities via mbstring is deprecated; use htmlspecialchars, htmlentities, or mb_encode_numericentity/mb_decode_numericentity <https://php-errors.readthedocs.io/en/latest/messages/handling-html-entities-via-mbstring-is-deprecated%3B-use-htmlspecialchars%2C-htmlentities%2C-or-mb_encode_numericentity-mb_decode_numericentity.html>`_
  + `Handling QPrint via mbstring is deprecated; use quoted_printable_encode/quoted_printable_decode <https://php-errors.readthedocs.io/en/latest/messages/handling-qprint-via-mbstring-is-deprecated%3B-use-quoted_printable_encode-quoted_printable_decode.html>`_
  + `Handling Uuencode via mbstring is deprecated; use convert_uuencode/convert_uudecode instead <https://php-errors.readthedocs.io/en/latest/messages/handling-uuencode-via-mbstring-is-deprecated%3B-use-convert_uuencode-convert_uudecode-instead.html>`_



Connex PHP features
-------------------

  + `encoding <https://php-dictionary.readthedocs.io/en/latest/dictionary/encoding.ini.html>`_


Suggestions
___________

* Use uuencode() and uudecode() functions.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DeprecatedMbEncoding                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP82 <ruleset-CompatibilityPHP82>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


