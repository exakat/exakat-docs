.. _php-castunsetusage:


.. _cast-(unset)-usage:

Cast (unset) Usage
++++++++++++++++++

.. meta::
	:description:
		Cast (unset) Usage: This rule reports usage of the ``(unset)`` cast operator.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Cast (unset) Usage
	:twitter:description: Cast (unset) Usage: This rule reports usage of the ``(unset)`` cast operator
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Cast (unset) Usage
	:og:type: article
	:og:description: This rule reports usage of the ``(unset)`` cast operator
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Cast (unset) Usage.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/CastUnsetUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/CastUnsetUsage.html","name":"Cast (unset) Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 11 Feb 2025 09:13:38 +0000","dateModified":"Tue, 11 Feb 2025 09:13:38 +0000","description":"This rule reports usage of the ``(unset)`` cast operator","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Cast (unset) Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports usage of the ``(unset)`` cast operator. The operator was removed in PHP 8.0. The operator was deprecated since PHP 7.2.0.

.. code-block:: php
   
   <?php
   
   $a = 1;
   (unset) $a;
   
   // functioncall is OK
   unset($a);
   
   ?>

See also `Unset casting <https://www.php.net/manual/en/language.types.null.php#language.types.null.casting>`_.

Related PHP errors 
-------------------

  + `The (unset) cast is no longer supported <https://php-errors.readthedocs.io/en/latest/messages/the-%28unset%29-cast-is-no-longer-supported.html>`_
  + `The (unset) cast is deprecated <https://php-errors.readthedocs.io/en/latest/messages/the-%28unset%29-cast-is-deprecated.html>`_



Connex PHP features
-------------------

  + `Cast Operator <https://php-dictionary.readthedocs.io/en/latest/dictionary/cast.ini.html>`_
  + `unset() <https://php-dictionary.readthedocs.io/en/latest/dictionary/unset.ini.html>`_


Suggestions
___________

* Replace `(unset)` with a call to unset().
* Remove the unset call altogether.
* Set the value to NULL.




Specs
_____

+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/CastUnsetUsage                                                                                                                                                                      |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>`                                                                                |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 2.1.8                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 8.0 and older                                                                                                                                                                  |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                                                                         |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.0 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/unset_cast.html>`__                                                                                    |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                               |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


