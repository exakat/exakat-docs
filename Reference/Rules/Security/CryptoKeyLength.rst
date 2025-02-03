.. _security-cryptokeylength:


.. _check-crypto-key-length:

Check Crypto Key Length
+++++++++++++++++++++++

.. meta::
	:description:
		Check Crypto Key Length: Each cryptography algorithm requires a reasonable length.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Check Crypto Key Length
	:twitter:description: Check Crypto Key Length: Each cryptography algorithm requires a reasonable length
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Check Crypto Key Length
	:og:type: article
	:og:description: Each cryptography algorithm requires a reasonable length
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Check Crypto Key Length.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/CryptoKeyLength.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/CryptoKeyLength.html","name":"Check Crypto Key Length","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Each cryptography algorithm requires a reasonable length","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Check Crypto Key Length.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Each cryptography algorithm requires a reasonable length. Make sure an up-to-date length is used. 

This rule use the following recommendations : 

+ `OPENSSL_KEYTYPE_RSA` => 3072
+ `OPENSSL_KEYTYPE_DSA` => 2048
+ `OPENSSL_KEYTYPE_DH`  => 2048
+ `OPENSSL_KEYTYPE_EC`  => 512

The values above are used with the openssl PHP extension.

.. code-block:: php
   
   <?php
   
   // Extracted from the documentation
   
   // Generates a new and strong key 
   $private_key = openssl_pkey_new(array(
       "private_key_type" => OPENSSL_KEYTYPE_EC,
       "private_key_bits" => 1024,
   ));
   
   // Generates a new and weak key 
   $private_key = openssl_pkey_new(array(
       "private_key_type" => OPENSSL_KEYTYPE_EC,
       "private_key_bits" => 256,
   ));
   
   ?>

See also `The Definitive 2019 Guide to Cryptographic Key Sizes and Algorithm Recommendations <https://paragonie.com/blog/2019/03/definitive-2019-guide-cryptographic-key-sizes-and-algorithm-recommendations>`_ and `Cryptographic Key Length Recommendation <https://www.keylength.com/>`_.

Connex PHP features
-------------------

  + `cryptography <https://php-dictionary.readthedocs.io/en/latest/dictionary/cryptography.ini.html>`_
  + `openssl <https://php-dictionary.readthedocs.io/en/latest/dictionary/openssl.ini.html>`_


Suggestions
___________

* Lengthen the cryptographic key




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/CryptoKeyLength                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.1                                                                                                                   |
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


