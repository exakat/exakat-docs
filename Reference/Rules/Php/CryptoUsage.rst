.. _php-cryptousage:


.. _crypto-usage:

Crypto Usage
++++++++++++

.. meta::
	:description:
		Crypto Usage: Usage of cryptography and hashes functions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Crypto Usage
	:twitter:description: Crypto Usage: Usage of cryptography and hashes functions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Crypto Usage
	:og:type: article
	:og:description: Usage of cryptography and hashes functions
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Crypto Usage.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/CryptoUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/CryptoUsage.html","name":"Crypto Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Usage of cryptography and hashes functions","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Crypto Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Usage of cryptography and hashes functions. 

The functions listed are the native PHP functions, and do not belong to a specific extension, like ``OpenSSL``, ``mcrypt`` or ``mhash``.

Cryptography and hashes are mainly used for storing sensitive data, such as passwords, or to verify authenticity of data. They may also be used for name-randomization with cache.

.. code-block:: php
   
   <?php
   
   if (md5($_POST['password']) === $row['password_hash']) {
       user_login($user);
   } else {
       error('Wrong password');
   }
   ?>

See also `Cryptography Extensions <https://www.php.net/manual/en/refs.crypto.php>`_.

Connex PHP features
-------------------

  + `crypto <https://php-dictionary.readthedocs.io/en/latest/dictionary/crypto.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/CryptoUsage                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.4                                                                                                                                                                                   |
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


