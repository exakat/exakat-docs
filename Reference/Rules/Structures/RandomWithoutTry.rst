.. _structures-randomwithouttry:


.. _random-without-try:

Random Without Try
++++++++++++++++++

.. meta::
	:description:
		Random Without Try: random_int() and random_bytes() require a try/catch structure around them.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Random Without Try
	:twitter:description: Random Without Try: random_int() and random_bytes() require a try/catch structure around them
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Random Without Try
	:og:type: article
	:og:description: random_int() and random_bytes() require a try/catch structure around them
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Random Without Try.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/RandomWithoutTry.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/RandomWithoutTry.html","name":"Random Without Try","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"random_int() and random_bytes() require a try\/catch structure around them","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Random Without Try.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`random_int() <https://www.php.net/random_int>`_ and `random_bytes() <https://www.php.net/random_bytes>`_ require a try/catch structure around them.

`random_int() <https://www.php.net/random_int>`_ and `random_bytes() <https://www.php.net/random_bytes>`_ emit Exceptions if they meet a problem. This way, failure can't be mistaken with returning an empty value, which leads to lower security. 
Since PHP 7.4, `openssl_random_pseudo_bytes() <https://www.php.net/openssl_random_pseudo_bytes>`_ has adopted the same behavior. It is included in this analysis : check your PHP version for actual application.

.. code-block:: php
   
   <?php
   
   try {
       $salt = random_bytes($length);
   } catch (TypeError $e) {
       // Error while reading the provided parameter
   } catch (Exception $e) {
       // Insufficient random data generated
   } catch (Error $e) {
       // Error with the provided parameter : <= 0
   }
   
   ?>
Connex PHP features
-------------------

  + `Random <https://php-dictionary.readthedocs.io/en/latest/dictionary/random.ini.html>`_


Suggestions
___________

* Add a try/catch structure around calls to random_int() and random_bytes().




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/RandomWithoutTry                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


