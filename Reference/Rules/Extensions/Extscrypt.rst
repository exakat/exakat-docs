.. _extensions-extscrypt:

.. _ext-scrypt:

ext/scrypt
++++++++++

.. meta::
	:description:
		ext/scrypt: This is a PHP library providing a wrapper to Colin Percival's scrypt implementation.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/scrypt
	:twitter:description: ext/scrypt: This is a PHP library providing a wrapper to Colin Percival's scrypt implementation
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/scrypt
	:og:type: article
	:og:description: This is a PHP library providing a wrapper to Colin Percival's scrypt implementation
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extscrypt.html
	:og:locale: en
This is a PHP library providing a wrapper to Colin Percival's scrypt implementation. Scrypt is a key derivation function designed to be far more `secure <https://www.php.net/secure>`_ against hardware brute-force attacks than alternative functions such as PBKDF2 or bcrypt.

.. code-block:: php
   
   <?php
   echo scrypt("", "", 16, 1, 1, 64) . "\n";
   echo scrypt("password", "NaCl", 1024, 8, 16, 64) . "\n";
   ?>

See also `scrypt <http://www.tarsnap.com/scrypt.html>` and `PHP scrypt module <https://github.com/DomBlack/php-scrypt>`.

Connex PHP features
-------------------

  + `crypto <https://php-dictionary.readthedocs.io/en/latest/dictionary/crypto.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extscrypt                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


