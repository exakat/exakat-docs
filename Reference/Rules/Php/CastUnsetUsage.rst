.. _php-castunsetusage:


.. _cast-unset-usage:

Cast Unset Usage
++++++++++++++++

.. meta::
	:description:
		Cast Unset Usage: Usage of the `(unset)` cast operator was removed.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Cast Unset Usage
	:twitter:description: Cast Unset Usage: Usage of the `(unset)` cast operator was removed
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Cast Unset Usage
	:og:type: article
	:og:description: Usage of the `(unset)` cast operator was removed
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Cast Unset Usage.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/CastUnsetUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/CastUnsetUsage.html","name":"Cast Unset Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Usage of the `(unset)` cast operator was removed","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Cast Unset Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Usage of the `(unset)` cast operator was removed. The operator was deprecated since PHP 7.2.0.

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

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/CastUnsetUsage                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>`                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.8                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


