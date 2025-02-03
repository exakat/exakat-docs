.. _structures-cryptwithoutsalt:


.. _crypt()-without-salt:

crypt() Without Salt
++++++++++++++++++++


.. meta::

	:description:

		crypt() Without Salt: PHP requires a salt when calling crypt().

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: crypt() Without Salt

	:twitter:description: crypt() Without Salt: PHP requires a salt when calling crypt()

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: crypt() Without Salt

	:og:type: article

	:og:description: PHP requires a salt when calling crypt()

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/crypt() Without Salt.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CryptWithoutSalt.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CryptWithoutSalt.html","name":"crypt() Without Salt","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"PHP requires a salt when calling crypt()","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/crypt() Without Salt.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PHP requires a salt when calling `crypt() <https://www.php.net/crypt>`_. 5.5 and previous versions didn't require it. Salt is a simple string, that is usually only known by the application.

According to the manual : The salt parameter is optional. However, `crypt() <https://www.php.net/crypt>`_ creates a weak hash without the salt. PHP 5.6 or later raise an `E_NOTICE <https://www.php.net/E_NOTICE>`_ `error <https://www.php.net/error>`_ without it. Make sure to specify a strong enough salt for better security.

.. code-block:: php
   
   <?php
   // Set the password
   $password = 'mypassword';
   
   // salted crypt usage (always valid)
   $hash = crypt($password, '123salt');
   
   // Get the hash, letting the salt be automatically generated
   // This generates a notice after PHP 5.6
   $hash = crypt($password);
   
   ?>

See also `crypt <http://www.php.net/crypt>`_.


Suggestions
___________

* Always provide the second argument




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Structures/CryptWithoutSalt                                                                                                          |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 5.6 and older                                                                                                               |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Instant (5 mins)                                                                                                                     |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 5.6                                                                                                                              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                            |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+


