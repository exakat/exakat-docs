.. _php-nonullfornative:


.. _no-null-for-native-php-functions:

No Null For Native PHP Functions
++++++++++++++++++++++++++++++++

.. meta::
	:description:
		No Null For Native PHP Functions: Null is not acceptable anymore as an argument, for PHP native functions that require a non-nullable argument.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Null For Native PHP Functions
	:twitter:description: No Null For Native PHP Functions: Null is not acceptable anymore as an argument, for PHP native functions that require a non-nullable argument
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Null For Native PHP Functions
	:og:type: article
	:og:description: Null is not acceptable anymore as an argument, for PHP native functions that require a non-nullable argument
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Null For Native PHP Functions.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/NoNullForNative.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/NoNullForNative.html","name":"No Null For Native PHP Functions","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"Null is not acceptable anymore as an argument, for PHP native functions that require a non-nullable argument","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Null For Native PHP Functions.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Null is not acceptable anymore as an argument, for PHP native functions that require a non-nullable argument.

Until PHP 8.1, it was magically turned into an empty string.

.. code-block:: php
   
   <?php
   
   $haystack = 'abc';
   // $needle was omitted...
   echo strpos($haystack, $needle);
   
   ?>

See also `PHP RFC: Deprecate passing null to non-nullable arguments of internal functions <https://wiki.php.net/rfc/deprecate_null_to_scalar_internal_arg>`_.

Related PHP errors 
-------------------

  + `Passing null to parameter #%d ($%s) of type %s is deprecated <https://php-errors.readthedocs.io/en/latest/messages/%25s%28%29%3A-passing-null-to-parameter-%23%25.html>`_



Connex PHP features
-------------------

  + `null <https://php-dictionary.readthedocs.io/en/latest/dictionary/null.ini.html>`_


Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/NoNullForNative                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>`, :ref:`Deprecated <ruleset-Deprecated>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.5                                                                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                                                                                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                           |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


