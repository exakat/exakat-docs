.. _attributes-nestedattributes:


.. _nested-attributes:

Nested Attributes
+++++++++++++++++

.. meta::
	:description:
		Nested Attributes: Nested attribute are attribute in attributes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Nested Attributes
	:twitter:description: Nested Attributes: Nested attribute are attribute in attributes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Nested Attributes
	:og:type: article
	:og:description: Nested attribute are attribute in attributes
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Nested Attributes.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Attributes\/NestedAttributes.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Attributes\/NestedAttributes.html","name":"Nested Attributes","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 14 Jan 2025 12:52:58 +0000","dateModified":"Tue, 14 Jan 2025 12:52:58 +0000","description":"Nested attribute are attribute in attributes","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Nested Attributes.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Nested `attribute <https://www.php.net/attribute>`_ are `attribute <https://www.php.net/attribute>`_ in attributes. 
Nested attributes are not available in PHP 8.0 and older. It is reported as an invalid constant expression.

.. code-block:: php
   
   <?php
   // Extracted from PHP 8.1 addendum (https://www.php.net/releases/8.1/en.php#new_in_initializers)
   class User
   {
       #[\Assert\All(
           new \Assert\NotNull,
           new \Assert\Length(min: 6))
       ]
       public string $name = '';
   }
   ?>

See also `PHP RFC: New in initializers <https://wiki.php.net/rfc/new_in_initializers>`_ and `New initializers`.

Related PHP errors 
-------------------

  + `Constant expression contains invalid operations <https://php-errors.readthedocs.io/en/latest/messages/constant-expression-contains-invalid-operations.html>`_



Connex PHP features
-------------------

  + `new-in-initializer <https://php-dictionary.readthedocs.io/en/latest/dictionary/new-in-initializer.ini.html>`_
  + `nested-attribute <https://php-dictionary.readthedocs.io/en/latest/dictionary/nested-attribute.ini.html>`_


Specs
_____

+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Attributes/NestedAttributes                                                                                                                                                                                                                                                            |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP73 <ruleset-CompatibilityPHP73>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>` |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 2.3.1                                                                                                                                                                                                                                                                                  |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 8.1 and more recent                                                                                                                                                                                                                                                           |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         |                                                                                                                                                                                                                                                                                        |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      |                                                                                                                                                                                                                                                                                        |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.1 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/nestedAttributes.html>`__                                                                                                                                                                             |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                                                                                                                              |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


