.. _php-php56newfunctions:

.. _new-functions-in-php-5.6:

New Functions In PHP 5.6
++++++++++++++++++++++++

.. meta::
	:description:
		New Functions In PHP 5.6: PHP introduced new functions in PHP 5.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: New Functions In PHP 5.6
	:twitter:description: New Functions In PHP 5.6: PHP introduced new functions in PHP 5
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: New Functions In PHP 5.6
	:og:type: article
	:og:description: PHP introduced new functions in PHP 5
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/New Functions In PHP 5.6.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php56NewFunctions.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php56NewFunctions.html","name":"New Functions In PHP 5.6","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"PHP introduced new functions in PHP 5","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/New Functions In PHP 5.6.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>PHP introduced new functions in PHP 5.6. If you have already defined functions with such names, you will get a conflict when trying to upgrade. It is advised to change those functions' name.

+ `gmp_root() <https://www.php.net/gmp_root>`_
+ `gmp_rootrem() <https://www.php.net/gmp_rootrem>`_
+ `ldap_escape() <https://www.php.net/ldap_escape>`_
+ `oci_get_implicit_resultset() <https://www.php.net/oci_get_implicit_resultset>`_
+ `openssl_x509_fingerprint() <https://www.php.net/openssl_x509_fingerprint>`_
+ `openssl_spki_new() <https://www.php.net/openssl_spki_new>`_
+ `openssl_spki_verify() <https://www.php.net/openssl_spki_verify>`_
+ `openssl_spki_export_challenge() <https://www.php.net/openssl_spki_export_challenge>`_
+ `openssl_spki_export() <https://www.php.net/openssl_spki_export>`_

Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php56NewFunctions                                                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.6 and older                                                                                                                                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


