.. _security-minusoneonerror:


.. _minus-one-on-error:

Minus One On Error
++++++++++++++++++

.. meta::
	:description:
		Minus One On Error: Several PHP native functions return -1 on error.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Minus One On Error
	:twitter:description: Minus One On Error: Several PHP native functions return -1 on error
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Minus One On Error
	:og:type: article
	:og:description: Several PHP native functions return -1 on error
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Minus One On Error.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/MinusOneOnError.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/MinusOneOnError.html","name":"Minus One On Error","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Several PHP native functions return -1 on error","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Minus One On Error.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Several PHP native functions return -1 on `error <https://www.php.net/error>`_. They also return 1 in case of success, and 0 in case of failure. This leads to confusions.

In case the native function is used as a condition without explicit comparison, PHP type cast the return value to a boolean. In this case, -1 and 1 are both converted to `true <https://www.php.net/true>`_, and the condition applies. This means that an `error <https://www.php.net/error>`_ situation is mistaken for a successful event. 
This analysis searches for if/then structures, ternary operators inside `while() <https://www.php.net/manual/en/control-structures.while.php>`_ / do...`while() <https://www.php.net/manual/en/control-structures.while.php>`_ loops.

.. code-block:: php
   
   <?php
   
   // Proper check of the return value
   if (openssl_verify($data, $signature, $public) === 1) {
       $this->loginAsUser($user);
   }
   
   // if this call fails, it returns -1, and is confused with true
   if (openssl_verify($data, $signature, $public)) {
       $this->loginAsUser($user);
   }
   ?>

See also `Can you spot the vulnerability? (openssl_verify) <https://twitter.com/ripstech/status/1124325237967994880>`_ and `Incorrect Signature Verification <https://snyk.io/vuln/SNYK-PHP-SIMPLESAMLPHPSIMPLESAMLPHPMODULEINFOCARD-70167>`_.


Suggestions
___________

* Compare explicitly the return value to 1




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/MinusOneOnError                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


