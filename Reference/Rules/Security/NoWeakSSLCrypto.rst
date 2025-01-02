.. _security-noweaksslcrypto:

.. _no-weak-ssl-crypto:

No Weak SSL Crypto
++++++++++++++++++

.. meta::
	:description:
		No Weak SSL Crypto: When enabling PHP's stream SSL, it is important to use a safe protocol.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Weak SSL Crypto
	:twitter:description: No Weak SSL Crypto: When enabling PHP's stream SSL, it is important to use a safe protocol
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Weak SSL Crypto
	:og:type: article
	:og:description: When enabling PHP's stream SSL, it is important to use a safe protocol
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Weak SSL Crypto.html
	:og:locale: en
When enabling PHP's stream SSL, it is important to use a safe protocol. 

All the SSL protocols (1.0, 2.0, 3.0), and TLS (1.0 are unsafe. The best is to use the most recent TLS, version 1.2. 

`stream_socket_enable_crypto() <https://www.php.net/stream_socket_enable_crypto>`_ and `curl_setopt() <https://www.php.net/curl_setopt>`_ are checked.
Using the TLS transport protocol of PHP will choose the version by itself.

.. code-block:: php
   
   <?php
   
   // This socket will use SSL v2, which 
   $socket = 'sslv2://www.example.com';
   $fp = fsockopen($socket, 80, $errno, $errstr, 30);
   
   ?>

See also `Insecure Transportation Security Protocol Supported (TLS 1.0) <https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/insecure-transportation-security-protocol-supported-tls-10/>`_, `The 2018 Guide to Building Secure PHP Software <https://paragonie.com/blog/2017/12/2018-guide-building-secure-php-software>`_ and `Internet Domain: TCP, UDP, SSL, and TLS <https://www.php.net/manual/en/transports.inet.php>`_.

Connex PHP features
-------------------

  + `ssl <https://php-dictionary.readthedocs.io/en/latest/dictionary/ssl.ini.html>`_


Suggestions
___________

* Use TLS transport, with version 1.2




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/NoWeakSSLCrypto                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


