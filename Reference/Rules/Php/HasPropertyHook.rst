.. _php-haspropertyhook:


.. _has-property-hook:

Has Property Hook
+++++++++++++++++

.. meta::
	:description:
		Has Property Hook: The analyzed code makes use of property hooks.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Has Property Hook
	:twitter:description: Has Property Hook: The analyzed code makes use of property hooks
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Has Property Hook
	:og:type: article
	:og:description: The analyzed code makes use of property hooks
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Has Property Hook.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/HasPropertyHook.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/HasPropertyHook.html","name":"Has Property Hook","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"The analyzed code makes use of property hooks","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Has Property Hook.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The analyzed code makes use of property hooks. Property hooks are special methods, ``get`` and ``set``, which are called when a property is read or written. 

Property hooks were introduced in PHP 8.4.

.. code-block:: php
   
   <?php
   
   class x {
   	private string $property {
   		get => $this->property;
   		
   		set { $this->property = mb_strtolower($property);}
   	}
   }
   
   ?>
Connex PHP features
-------------------

  + `Array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/HasPropertyHook                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CompatibilityPHP84 <ruleset-CompatibilityPHP84>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.8                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.4 and more recent                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


