.. _php-php84newfunctions:

.. _new-functions-in-php-8.4:

New Functions In PHP 8.4
++++++++++++++++++++++++

.. meta::
	:description:
		New Functions In PHP 8.4: New functions are added to new PHP version.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: New Functions In PHP 8.4
	:twitter:description: New Functions In PHP 8.4: New functions are added to new PHP version
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: New Functions In PHP 8.4
	:og:type: article
	:og:description: New functions are added to new PHP version
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/Php84NewFunctions.html
	:og:locale: en
New functions are added to new PHP version.

The following functions are now native functions in PHP 8.4. It is compulsory to rename any custom function that was created in older versions. One alternative is to move the function to a custom namespace, and update the use list at the beginning of the script. 

* \`exit() <https://www.www.php.net/exit>`_
* \`die() <https://www.php.net/die>`_
* \bcfloor()
* \bcceil()
* \bcround()
* \dom\import_simplexml()
* \grapheme_str_split()
* \intltz_get_iana_id()
* \mb_ucfirst()
* \mb_lcfirst()
* \mb_trim()
* \mb_ltrim()
* \mb_rtrim()
* \array_find()
* \array_find_key()
* \array_any()
* \array_all()
* \http_get_last_response_headers()
* \http_clear_last_response_headers()
* \request_parse_body()
* \fpow()
* \pcntl_waitid()
* \pcntl_getqos_class()
* \pcntl_setqos_class()
* \pg_jit()
* \pg_result_memory_size()
* \pg_change_password()
* \pg_put_copy_data()
* \pg_put_copy_end()
* \pg_socket_poll()
* \sodium_crypto_aead_aes256gcm_decrypt()
* \sodium_crypto_aead_aes256gcm_encrypt()
* \sodium_crypto_aead_aes256gcm_keygen()
* \sodium_crypto_aead_aegis128l_decrypt()
* \sodium_crypto_aead_aegis128l_encrypt()
* \sodium_crypto_aead_aegis128l_keygen()
* \sodium_crypto_aead_aegis256_decrypt()
* \sodium_crypto_aead_aegis256_encrypt()
* \sodium_crypto_aead_aegis256_keygen()



.. code-block:: php
   
   <?php
   
   // checks that ALL elements satisfy the closure
   array_all(
       ['1', 'A', '-12'],
       is_numeric(...),
   );
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php84NewFunctions                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.4 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


