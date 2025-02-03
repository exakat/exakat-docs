.. _php-opensslencryptalgochange:


.. _openssl-encrypt-default-algorithm-change:

Openssl Encrypt Default Algorithm Change
++++++++++++++++++++++++++++++++++++++++


.. meta::

	:description:

		Openssl Encrypt Default Algorithm Change: openssl_pkcs7_encrypt() and openssl_cms_encrypt() will now default to using AES-128-CBC rather than RC2-40.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Openssl Encrypt Default Algorithm Change

	:twitter:description: Openssl Encrypt Default Algorithm Change: openssl_pkcs7_encrypt() and openssl_cms_encrypt() will now default to using AES-128-CBC rather than RC2-40

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Openssl Encrypt Default Algorithm Change

	:og:type: article

	:og:description: openssl_pkcs7_encrypt() and openssl_cms_encrypt() will now default to using AES-128-CBC rather than RC2-40

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Openssl Encrypt Default Algorithm Change.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/OpensslEncryptAlgoChange.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/OpensslEncryptAlgoChange.html","name":"Openssl Encrypt Default Algorithm Change","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"openssl_pkcs7_encrypt() and openssl_cms_encrypt() will now default to using AES-128-CBC rather than RC2-40","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Openssl Encrypt Default Algorithm Change.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`openssl_pkcs7_encrypt() <https://www.php.net/openssl_pkcs7_encrypt>`_ and `openssl_cms_encrypt() <https://www.php.net/openssl_cms_encrypt>`_ will now default to using AES-128-CBC rather than RC2-40. The RC2-40 cipher is considered insecure and not enabled by default in OpenSSL 3.

This means that the default argument of `OPENSSL_CIPHER_RC2_40 <https://www.php.net/OPENSSL_CIPHER_RC2_40>`_ is replaced by `OPENSSL_CIPHER_AES_128_CBC <https://www.php.net/OPENSSL_CIPHER_AES_128_CBC>`_.

.. code-block:: php
   
   <?php
   // extracted from the PHP documentation
   // encrypt it
   if (openssl_pkcs7_encrypt("msg.txt", "enc.txt", $key,
       array("To" => "nighthawk@example.com", // keyed syntax
             "From: HQ <hq@example.com>", // indexed syntax
             "Subject" => "Eyes only"))) {
       // message encrypted - send it!
       exec(ini_get("sendmail_path") . " < enc.txt");
   }
   ?>
Connex PHP features
-------------------

  + `cryptography <https://php-dictionary.readthedocs.io/en/latest/dictionary/cryptography.ini.html>`_
  + `openssl <https://php-dictionary.readthedocs.io/en/latest/dictionary/openssl.ini.html>`_


Suggestions
___________

* Explicitly set the 5th and 6th argument of the functioncalls to avoid a disruption.
* Update the target service to handle the new cipher algorithm.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/OpensslEncryptAlgoChange                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.3                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


