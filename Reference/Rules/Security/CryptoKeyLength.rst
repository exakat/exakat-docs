.. _security-cryptokeylength:

.. _check-crypto-key-length:

Check Crypto Key Length
+++++++++++++++++++++++

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


Suggestions
___________

* Lengthen the cryptographic key




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/CryptoKeyLength                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Security <ruleset-Security>`                                                            |
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
| Features     | cryptography, openssl                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


