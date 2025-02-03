.. _extensions-extcrypto:


.. _ext-crypto:

ext/crypto
++++++++++


.. meta::

	:description:

		ext/crypto: Extension ext/crypto (PECL).

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: ext/crypto

	:twitter:description: ext/crypto: Extension ext/crypto (PECL)

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: ext/crypto

	:og:type: article

	:og:description: Extension ext/crypto (PECL)

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/crypto.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extcrypto.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extcrypto.html","name":"ext\/crypto","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension ext\/crypto (PECL)","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/crypto.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension ext/crypto (PECL).

Objective PHP binding of OpenSSL Crypto library.

.. code-block:: php
   
   <?php
   use Crypto\Cipher;
   use Crypto\AlgorihtmException;
   $algorithm = 'aes-256-cbc';
   if (!Cipher::hasAlgorithm($algorithm)) {
   	die('Algorithm $algorithm not found' . PHP_EOL);
   }
   try {
   	$cipher = new Cipher($algorithm);
   	// Algorithm method for retrieving algorithm
   	echo 'Algorithm: ' . $cipher->getAlgorithmName() . PHP_EOL;
   	// Params
   	$key_len = $cipher->getKeyLength();
   	$iv_len = $cipher->getIVLength();
   	
   	echo 'Key length: ' . $key_len . PHP_EOL;
   	echo 'IV length: '  . $iv_len . PHP_EOL;
   	echo 'Block size: ' . $cipher->getBlockSize() . PHP_EOL;
   	// This is just for this example. You should never use such key and IV!
   	$key = str_repeat('x', $key_len);
   	$iv = str_repeat('i', $iv_len);
   	// Test data
   	$data1 = 'Test';
   	$data2 = 'Data';
   	$data = $data1 . $data2;
   	// Simple encryption
   	$sim_ct = $cipher->encrypt($data, $key, $iv);
   	
   	// init/update/finish encryption
   	$cipher->encryptInit($key, $iv);
   	$iuf_ct  = $cipher->encryptUpdate($data1);
   	$iuf_ct .= $cipher->encryptUpdate($data2);
   	$iuf_ct .= $cipher->encryptFinish();
   	// Raw data output (used base64 format for printing)
   	echo 'Ciphertext (sim): ' . base64_encode($sim_ct) . PHP_EOL;
   	echo 'Ciphertext (iuf): ' . base64_encode($iuf_ct) . PHP_EOL;
   	// $iuf_out == $sim_out
   	$ct = $sim_ct;
   	// Another way how to create a new cipher object (using the same algorithm and mode)
   	$cipher = Cipher::aes(Cipher::MODE_CBC, 256);
   	// Simple decryption
   	$sim_text = $cipher->decrypt($ct, $key, $iv);
   	
   	// init/update/finish decryption
   	$cipher->decryptInit($key, $iv);
   	$iuf_text = $cipher->decryptUpdate($ct);
   	$iuf_text .= $cipher->decryptFinish();
   	// Raw data output ($iuf_out == $sim_out)
   	echo 'Text (sim): ' . $sim_text . PHP_EOL;
   	echo 'Text (iuf): ' . $iuf_text . PHP_EOL;
   }
   catch (AlgorithmException $e) {
   	echo $e->getMessage() . PHP_EOL;
   }
   
   ?>

See also `pecl crypto <https://pecl.php.net/package/crypto>`_ and `php-crypto <https://github.com/bukka/php-crypto>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extcrypto                                                                                                                                                                    |
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


