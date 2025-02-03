.. _extensions-extpkcs11:


.. _ext-pkcs11:

ext/pkcs11
++++++++++

.. meta::
	:description:
		ext/pkcs11: In cryptography, PKCS #11 is one of the Public-Key Cryptography Standards.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/pkcs11
	:twitter:description: ext/pkcs11: In cryptography, PKCS #11 is one of the Public-Key Cryptography Standards
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/pkcs11
	:og:type: article
	:og:description: In cryptography, PKCS #11 is one of the Public-Key Cryptography Standards
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/pkcs11.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extpkcs11.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extpkcs11.html","name":"ext\/pkcs11","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"In cryptography, PKCS #11 is one of the Public-Key Cryptography Standards","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/pkcs11.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

In cryptography, PKCS #11 is one of the Public-Key Cryptography Standards. This extensions provides methods to create, read and check those keys.

.. code-block:: php
   
   <?php
   
   $key = $session->generateKey(new Pkcs11\Mechanism(Pkcs11\CKM_AES_KEY_GEN), [
     Pkcs11\CKA_CLASS => Pkcs11\CKO_SECRET_KEY,
     Pkcs11\CKA_SENSITIVE => true,
     Pkcs11\CKA_ENCRYPT => true,
     Pkcs11\CKA_DECRYPT => true,
     Pkcs11\CKA_VALUE_LEN => 32,
     Pkcs11\CKA_KEY_TYPE => Pkcs11\CKK_AES,
     Pkcs11\CKA_LABEL => "Test AES",
     Pkcs11\CKA_PRIVATE => true,
   ]);
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extpkcs11                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


