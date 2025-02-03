.. _complete-extendedtypehints:


.. _extended-types:

Extended Types
++++++++++++++

.. meta::
	:description:
		Extended Types: Produces all the definition links between typehints (arguments, return types, properties) and the definitions that are valid with the type.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Extended Types
	:twitter:description: Extended Types: Produces all the definition links between typehints (arguments, return types, properties) and the definitions that are valid with the type
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Extended Types
	:og:type: article
	:og:description: Produces all the definition links between typehints (arguments, return types, properties) and the definitions that are valid with the type
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Extended Types.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/ExtendedTypehints.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/ExtendedTypehints.html","name":"Extended Types","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 24 Jan 2025 10:21:35 +0000","dateModified":"Fri, 24 Jan 2025 10:21:35 +0000","description":"Produces all the definition links between typehints (arguments, return types, properties) and the definitions that are valid with the type","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Extended Types.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Produces all the definition links between typehints (arguments, return types, properties) and the definitions that are valid with the type.

.. code-block:: php
   
   <?php
   
   function foo(A $A) {}
   
   // This is the raw definition of the above type
   interface A {}
   
   // This is valid definition of the above type
   class X implements A {}
   // This is valid definition of the above type
   class Y extends X {}
   
   // This is not related to the type
   class Z {}
   
   ?>
Connex PHP features
-------------------

  + `type <https://php-dictionary.readthedocs.io/en/latest/dictionary/type.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/ExtendedTypehints                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


