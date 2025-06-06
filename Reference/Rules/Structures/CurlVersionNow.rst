.. _structures-curlversionnow:


.. _curl\_version()-has-no-argument:

curl_version() Has No Argument
++++++++++++++++++++++++++++++

.. meta::
	:description:
		curl_version() Has No Argument: curl_version() used to accept ``CURLVERSION_NOW`` as argument.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: curl_version() Has No Argument
	:twitter:description: curl_version() Has No Argument: curl_version() used to accept ``CURLVERSION_NOW`` as argument
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: curl_version() Has No Argument
	:og:type: article
	:og:description: curl_version() used to accept ``CURLVERSION_NOW`` as argument
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/curl_version() Has No Argument.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CurlVersionNow.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CurlVersionNow.html","name":"curl_version() Has No Argument","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"curl_version() used to accept ``CURLVERSION_NOW`` as argument","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/curl_version() Has No Argument.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`curl_version() <https://www.php.net/curl_version>`_ used to accept ``CURLVERSION_NOW`` as argument. Since PHP 7.4, it is a function without arguments.

.. code-block:: php
   
   <?php
   
   // Compatible syntax
   $details = curl_version(CURLVERSION_NOW);
   
   // New PHP 7.4 syntax
   $details = curl_version();
   
   ?>

See also `curl_version <https://www.php.net/manual/en/function.curl-version.php>`_.


Suggestions
___________

* Drop all arguments from curl_version() calls.




Specs
_____

+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Structures/CurlVersionNow                                                                                                                                                               |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`                            |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 1.8.4                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                                                                                     |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                                                                         |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.4                                                                                                                                                                                 |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                               |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


