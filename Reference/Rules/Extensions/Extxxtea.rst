.. _extensions-extxxtea:

.. _ext-xxtea:

ext/xxtea
+++++++++

.. meta::
	:description:
		ext/xxtea: Extension xxtea : XXTEA encryption algorithm extension for PHP.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/xxtea
	:twitter:description: ext/xxtea: Extension xxtea : XXTEA encryption algorithm extension for PHP
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/xxtea
	:og:type: article
	:og:description: Extension xxtea : XXTEA encryption algorithm extension for PHP
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extxxtea.html
	:og:locale: en
Extension xxtea : XXTEA encryption algorithm extension for PHP.

XXTEA is a fast and `secure <https://www.php.net/secure>`_ encryption algorithm. This is a XXTEA extension for PHP.
It is different from the original XXTEA encryption algorithm. It encrypts and decrypts string instead of uint32 array, and the key is also string.

.. code-block:: php
   
   <?php
   // Example is extracted from the xxtea repository on github : tests/xxtea.phpt
   
   $str = 'Hello World! 你好，中国🇨🇳！';
   $key = '1234567890';
   $base64 = 'D4t0rVXUDl3bnWdERhqJmFIanfn/6zAxAY9jD6n9MSMQNoD8TOS4rHHcGuE=';
   $encrypt_data = xxtea_encrypt($str, $key);
   $decrypt_data = xxtea_decrypt($encrypt_data, $key);
   if ($str == $decrypt_data && base64_encode($encrypt_data) == $base64) {
       echo 'success!';
   } else {
       echo base64_encode($encrypt_data);
       echo 'fail!';
   }
   ?>

See also `PECL ext/xxtea <https://pecl.php.net/package/xxtea>`_ and `ext/xxtea on Github <https://github.com/xxtea/xxtea-pecl>`_.

Connex PHP features
-------------------

  + `xxtea <https://php-dictionary.readthedocs.io/en/latest/dictionary/xxtea.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extxxtea                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.7                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


