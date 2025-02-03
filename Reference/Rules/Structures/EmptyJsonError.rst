.. _structures-emptyjsonerror:

.. _empty-json-error:

Empty Json Error
++++++++++++++++

.. meta::
	:description:
		Empty Json Error: json_last_error() keeps the last error that was generated while decoding a JSON string.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Empty Json Error
	:twitter:description: Empty Json Error: json_last_error() keeps the last error that was generated while decoding a JSON string
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Empty Json Error
	:og:type: article
	:og:description: json_last_error() keeps the last error that was generated while decoding a JSON string
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Empty Json Error.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/EmptyJsonError.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/EmptyJsonError.html","name":"Empty Json Error","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"json_last_error() keeps the last error that was generated while decoding a JSON string","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Empty Json Error.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>`json_last_error() <https://www.php.net/json_last_error>`_ keeps the last `error <https://www.php.net/error>`_ that was generated while decoding a JSON string. To reset this cache to empty, one must run a call to `json_decode() <https://www.php.net/json_decode>`_ that succeed. This leads some code to make an apparently pointless call, just to empty the `error <https://www.php.net/error>`_ cache, and avoid confusing the message with the one of a previous call.

.. code-block:: php
   
   <?php
   
   // This generates an error
   $json = json_decode([);
   
   $json = json_decode($valid_json);
   
   echo json_last_error(); // This error is confused for the last call, not the first one.
   
   // pointless call, except to empty the cache.
   $json = json_decode([]);
   
   $json = json_decode($valid_json);
   
   echo json_last_error(); // This error is dedicated to the last call
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/EmptyJsonError                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


