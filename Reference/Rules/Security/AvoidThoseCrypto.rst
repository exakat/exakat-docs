.. _security-avoidthosecrypto:


.. _avoid-those-hash-functions:

Avoid Those Hash Functions
++++++++++++++++++++++++++

.. meta::
	:description:
		Avoid Those Hash Functions: The following cryptography algorithms are considered insecure, and should be replaced with new and more modern algorithms.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Avoid Those Hash Functions
	:twitter:description: Avoid Those Hash Functions: The following cryptography algorithms are considered insecure, and should be replaced with new and more modern algorithms
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Avoid Those Hash Functions
	:og:type: article
	:og:description: The following cryptography algorithms are considered insecure, and should be replaced with new and more modern algorithms
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Avoid Those Hash Functions.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/AvoidThoseCrypto.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/AvoidThoseCrypto.html","name":"Avoid Those Hash Functions","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The following cryptography algorithms are considered insecure, and should be replaced with new and more modern algorithms","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Avoid Those Hash Functions.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The following cryptography algorithms are considered insecure, and should be replaced with new and more modern algorithms. 

``MD2``, ``MD4``, ``MD5``, ``SHA0``, ``SHA1``, ``CRC``, ``DES``, ``3DES``, ``RC2``, ``RC4``. 

When possible, avoid using them, may it be as PHP functions, or hashing function configurations (mcrypt, hash...).
Weak cryptography is commonly used for hashing values when caching them. In such cases, security is not a primary concern. However, it may later become such, when hackers get access to the cache folders, or if the cached identifier is published. As a preventive protection, it is recommended to always use a `secure <https://www.php.net/secure>`_ hashing function.

.. code-block:: php
   
   <?php
   
   // Weak cryptographic algorithm
   echo md5('The quick brown fox jumped over the lazy dog.');
   
   // Weak cryptographic algorthim, used with a modern PHP extension (easier to update)
   echo hash('md5', 'The quick brown fox jumped over the lazy dog.');
   
   // Strong cryptographic algorthim, used with a modern PHP extension
   echo hash('sha156', 'The quick brown fox jumped over the lazy dog.');
   
   ?>

See also `Secure Hash Algorithms <https://en.wikipedia.org/wiki/Secure_Hash_Algorithms>`_.

Connex PHP features
-------------------

  + `hash <https://php-dictionary.readthedocs.io/en/latest/dictionary/hash.ini.html>`_


Suggestions
___________

* Keep the current crypto, and add a call to a stronger one. 
* Change the crypto for a more modern one and update the related databases




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/AvoidThoseCrypto                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


