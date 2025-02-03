.. _functions-noreferencedvoid:

.. _no-referenced-void:

No Referenced Void
++++++++++++++++++

.. meta::
	:description:
		No Referenced Void: There is no point returning a reference with a void type.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Referenced Void
	:twitter:description: No Referenced Void: There is no point returning a reference with a void type
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Referenced Void
	:og:type: article
	:og:description: There is no point returning a reference with a void type
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Referenced Void.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/NoReferencedVoid.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/NoReferencedVoid.html","name":"No Referenced Void","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"There is no point returning a reference with a void type","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Referenced Void.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>There is no point returning a reference with a void type. This is now reported as deprecated in PHP 8.1.

.. code-block:: php
   
   <?php
   
   function &test(): void {}
   
   ?>

See also `PHP RFC: Deprecations for PHP 8.1 <https://wiki.php.net/rfc/deprecations_php_8_1>`_.

Related PHP errors 
-------------------

  + `Returning by reference from a void function is deprecated <https://php-errors.readthedocs.io/en/latest/messages/returning-by-reference-from-a-void-function-is-deprecated.html>`_



Connex PHP features
-------------------

  + `void <https://php-dictionary.readthedocs.io/en/latest/dictionary/void.ini.html>`_
  + `reference <https://php-dictionary.readthedocs.io/en/latest/dictionary/reference.ini.html>`_


Suggestions
___________

* Removes the reference operator from the function definition




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/NoReferencedVoid                                                                                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>`, :ref:`Deprecated <ruleset-Deprecated>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.4                                                                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                               |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


