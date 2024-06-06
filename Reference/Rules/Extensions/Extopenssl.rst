.. _extensions-extopenssl:

.. _ext-openssl:

ext/openssl
+++++++++++

  Extension Openssl.

This extension binds functions of ``OpenSSL`` library for symmetric and asymmetric encryption and decryption, ``PBKDF2``, ``PKCS7``, ``PKCS12``, ``X509`` and other cryptographic operations. In addition to that it provides implementation of ``TLS`` streams.

.. code-block:: php
   
   <?php
   // $data and $signature are assumed to contain the data and the signature
   
   // fetch public key from certificate and ready it
   $pubkeyid = openssl_pkey_get_public("file://src/openssl-0.9.6/demos/sign/cert.pem");
   
   // state whether signature is okay or not
   $ok = openssl_verify($data, $signature, $pubkeyid);
   if ($ok == 1) {
       echo "good";
   } elseif ($ok == 0) {
       echo "bad";
   } else {
       echo "ugly, error checking signature";
   }
   // free the key from memory
   openssl_free_key($pubkeyid);
   ?>

See also `ext/OpenSSL <https://www.php.net/manual/en/book.openssl.php>`_ and `OpenSSL <https://www.openssl.org/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extopenssl                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
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


