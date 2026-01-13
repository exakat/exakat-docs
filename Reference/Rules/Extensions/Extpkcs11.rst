.. _extensions-extpkcs11:

.. _ext-pkcs11:

ext/pkcs11
++++++++++

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


