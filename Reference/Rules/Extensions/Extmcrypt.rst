.. _extensions-extmcrypt:


.. _ext-mcrypt:

ext/mcrypt
++++++++++

.. meta::
	:description:
		ext/mcrypt: Extension for mcrypt.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/mcrypt
	:twitter:description: ext/mcrypt: Extension for mcrypt
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/mcrypt
	:og:type: article
	:og:description: Extension for mcrypt
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/mcrypt.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extmcrypt.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extmcrypt.html","name":"ext\/mcrypt","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension for mcrypt","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/mcrypt.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension for mcrypt.

This extension has been deprecated as of PHP 7.1.0 and moved to PECL as of PHP 7.2.0.

This is an interface to the mcrypt library, which supports a wide variety of block algorithms such as DES, TripleDES, Blowfish (default), 3-WAY, SAFER-SK64, SAFER-SK128, TWOFISH, TEA, RC2 and GOST in CBC, OFB, CFB and ECB cipher modes. Additionally, it supports RC6 and IDEA which are considered 'non-free'. CFB/OFB are 8bit by default.

.. code-block:: php
   
   <?php
       # --- ENCRYPTION ---
   
       # the key should be random binary, use scrypt, bcrypt or PBKDF2 to
       # convert a string into a key
       # key is specified using hexadecimal
       $key = pack('H*', 'bcb04b7e103a0cd8b54763051cef08bc55abe029fdebae5e1d417e2ffb2a00a3');
       
       # show key size use either 16, 24 or 32 byte keys for AES-128, 192
       # and 256 respectively
       $key_size =  strlen($key);
       echo 'Key size: ' . $key_size . PHP_EOL;
       
       $plaintext = 'This string was AES-256 / CBC / ZeroBytePadding encrypted.';
   
       # create a random IV to use with CBC encoding
       $iv_size = mcrypt_get_iv_size(MCRYPT_RIJNDAEL_128, MCRYPT_MODE_CBC);
       $iv = mcrypt_create_iv($iv_size, MCRYPT_RAND);
       
       # creates a cipher text compatible with AES (Rijndael block size = 128)
       # to keep the text confidential 
       # only suitable for encoded input that never ends with value 00h
       # (because of default zero padding)
       $ciphertext = mcrypt_encrypt(MCRYPT_RIJNDAEL_128, $key,
                                    $plaintext, MCRYPT_MODE_CBC, $iv);
   
       # prepend the IV for it to be available for decryption
       $ciphertext = $iv . $ciphertext;
       
       # encode the resulting cipher text so it can be represented by a string
       $ciphertext_base64 = base64_encode($ciphertext);
   
       echo  $ciphertext_base64 . PHP_EOL;
   
       # === WARNING ===
   
       # Resulting cipher text has no integrity or authenticity added
       # and is not protected against padding oracle attacks.
       
       # --- DECRYPTION ---
       
       $ciphertext_dec = base64_decode($ciphertext_base64);
       
       # retrieves the IV, iv_size should be created using mcrypt_get_iv_size()
       $iv_dec = substr($ciphertext_dec, 0, $iv_size);
       
       # retrieves the cipher text (everything except the $iv_size in the front)
       $ciphertext_dec = substr($ciphertext_dec, $iv_size);
   
       # may remove 00h valued characters from end of plain text
       $plaintext_dec = mcrypt_decrypt(MCRYPT_RIJNDAEL_128, $key,
                                       $ciphertext_dec, MCRYPT_MODE_CBC, $iv_dec);
       
       echo  $plaintext_dec . PHP_EOL;
   ?>

See also `extension mcrypt <http://www.php.net/manual/en/book.mcrypt.php>`_ and `mcrypt <http://mcrypt.sourceforge.net/>`_.

Connex PHP features
-------------------

  + `Cryptography <https://php-dictionary.readthedocs.io/en/latest/dictionary/crypto.ini.html>`_
  + `libsodium <https://php-dictionary.readthedocs.io/en/latest/dictionary/libsodium.ini.html>`_
  + `OpenSSL <https://php-dictionary.readthedocs.io/en/latest/dictionary/openssl.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extmcrypt                                                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP71 <ruleset-CompatibilityPHP71>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


