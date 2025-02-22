.. _type-opensslcipher:


.. _openssl-ciphers-used:

OpenSSL Ciphers Used
++++++++++++++++++++

.. meta::
	:description:
		OpenSSL Ciphers Used: List of all the OpenSSL ciphers used in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: OpenSSL Ciphers Used
	:twitter:description: OpenSSL Ciphers Used: List of all the OpenSSL ciphers used in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: OpenSSL Ciphers Used
	:og:type: article
	:og:description: List of all the OpenSSL ciphers used in the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/OpenSSL Ciphers Used.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/OpensslCipher.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/OpensslCipher.html","name":"OpenSSL Ciphers Used","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"List of all the OpenSSL ciphers used in the code","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/OpenSSL Ciphers Used.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

List of all the OpenSSL ciphers used in the code. 

It is important to always use valid cipher modes for SSL. In case of non-existent cipher, the cipher and decipher operation will not happen. Ciphers are marked as weak after their security is breached, and shall be removed from OpenSSL, and later, from PHP. 

By reviewing this inventory, it is possible to detect forgotten ciphers, and fix them.

The full list of available ciphers for the PHP installation is available with the function `openssl_get_cipher_methods() <https://www.php.net/openssl_get_cipher_methods>`_.

.. code-block:: php
   
   <?php
   // PHP documentation example, for PHP 7.1 and more recent
   //$key should have been previously generated in a cryptographically safe way, like openssl_random_pseudo_bytes
   $plaintext = "message to be encrypted";
   $cipher = "aes-128-gcm";
   if (in_array($cipher, openssl_get_cipher_methods()))
   {
       $ivlen = openssl_cipher_iv_length($cipher);
       $iv = openssl_random_pseudo_bytes($ivlen);
       $ciphertext = openssl_encrypt($plaintext, $cipher, $key, $options=0, $iv, $tag);
       //store $cipher, $iv, and $tag for decryption later
       $original_plaintext = openssl_decrypt($ciphertext, $cipher, $key, $options=0, $iv, $tag);
       echo $original_plaintext."\n";
   }
   ?>

See also openssl_encrypt() and `OpenSSL [PHP manual] <https://www.php.net/manual/en/book.openssl.php>`_.

Connex PHP features
-------------------

  + `OpenSSL <https://php-dictionary.readthedocs.io/en/latest/dictionary/openssl.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/OpensslCipher                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Inventory <ruleset-Inventory>`      |
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


