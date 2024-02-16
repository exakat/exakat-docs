.. _php-opensslencryptalgochange:

.. _openssl-encrypt-default-algorithm-change:

Openssl Encrypt Default Algorithm Change
++++++++++++++++++++++++++++++++++++++++

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

Suggestions
___________

* Explicitly set the 5th and 6th argument of the functioncalls to avoid a disruption.
* Update the target service to handle the new cipher algorithm.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/OpensslEncryptAlgoChange                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | cryptography, openssl                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


