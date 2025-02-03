.. _complete-setclassaliasdefinition:

.. _set-class\_alias()-definition:

Set class_alias() Definition
++++++++++++++++++++++++++++

.. meta::
	:description:
		Set class_alias() Definition: Links identifiers and nsname to the concrete class, interface, trait and enumeration when class_alias() was used to create the name.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Set class_alias() Definition
	:twitter:description: Set class_alias() Definition: Links identifiers and nsname to the concrete class, interface, trait and enumeration when class_alias() was used to create the name
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Set class_alias() Definition
	:og:type: article
	:og:description: Links identifiers and nsname to the concrete class, interface, trait and enumeration when class_alias() was used to create the name
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Set class_alias() Definition.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/SetClassAliasDefinition.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/SetClassAliasDefinition.html","name":"Set class_alias() Definition","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Links identifiers and nsname to the concrete class, interface, trait and enumeration when class_alias() was used to create the name","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Set class_alias() Definition.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Links identifiers and nsname to the concrete class, interface, trait and enumeration when `class_alias() <https://www.php.net/class_alias>`_ was used to create the name. The link is ``DEFINITION``.

`class_alias() <https://www.php.net/class_alias>`_ are detected at loading time, and are used unconditionally.

This means that the fully qualified name of the ``new`` call and the instantiated class may be different : without the alias, the fully qualified name is the current value, or its use's origin, while with `class_alias() <https://www.php.net/class_alias>`_, it is an arbitrary name.

.. code-block:: php
   
   <?php
   
   class x {
       public function foo() {}
   }
   
   class_alias('x', 'y');
   
   //y exists, as an alias of x.
   $y = new y;
   
   ?>
Connex PHP features
-------------------

  + `class-alias <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-alias.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/SetClassAliasDefinition                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`NoDoc <ruleset-NoDoc>`                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                   |
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


