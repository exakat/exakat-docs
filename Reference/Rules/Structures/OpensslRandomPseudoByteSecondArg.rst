.. _structures-opensslrandompseudobytesecondarg:


.. _openssl\_random\_pseudo\_byte()-second-argument:

openssl_random_pseudo_byte() Second Argument
++++++++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		openssl_random_pseudo_byte() Second Argument: openssl_random_pseudo_byte() uses exceptions to signal an error.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: openssl_random_pseudo_byte() Second Argument
	:twitter:description: openssl_random_pseudo_byte() Second Argument: openssl_random_pseudo_byte() uses exceptions to signal an error
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: openssl_random_pseudo_byte() Second Argument
	:og:type: article
	:og:description: openssl_random_pseudo_byte() uses exceptions to signal an error
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/openssl_random_pseudo_byte() Second Argument.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/OpensslRandomPseudoByteSecondArg.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/OpensslRandomPseudoByteSecondArg.html","name":"openssl_random_pseudo_byte() Second Argument","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"openssl_random_pseudo_byte() uses exceptions to signal an error","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/openssl_random_pseudo_byte() Second Argument.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

openssl_random_pseudo_byte() uses exceptions to signal an `error <https://www.php.net/error>`_. Since PHP 7.4, there is no need to use the second argument.

On the other hand, it is important to catch the `exception <https://www.php.net/exception>`_ that openssl_random_pseudo_byte() may emit.

.. code-block:: php
   
   <?php
       // PHP 7.4 way to check on random number generation
       try {
           $bytes = openssl_random_pseudo_bytes($i);
       } catch(\Exception $e) {
           die("Error while loading random number");
       }
   
       // Old way to check on random number generation
       $bytes = openssl_random_pseudo_bytes($i, $cstrong);
       if ($cstrong === false) {
           die("Error while loading random number");
       }
   ?>

See also `openssl_random_pseudo_byte <https://www.php.net/openssl_random_pseudo_bytes>`_ and `PHP RFC: Improve openssl_random_pseudo_bytes() <https://wiki.php.net/rfc/improve-openssl-random-pseudo-bytes>`_.

Connex PHP features
-------------------

  + `OpenSSL <https://php-dictionary.readthedocs.io/en/latest/dictionary/openssl.ini.html>`_


Suggestions
___________

* Skip the second argument, add a try/catch around the call to openssl_random_pseudo_bytes()




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/OpensslRandomPseudoByteSecondArg                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.3                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


