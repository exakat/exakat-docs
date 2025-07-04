.. _attributes-deprecated:


.. _deprecated-attribute:

Deprecated Attribute
++++++++++++++++++++

.. meta::
	:description:
		Deprecated Attribute: The Deprecated attribute marks a class, method, property, class constants and functions that should not be used anymore.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Deprecated Attribute
	:twitter:description: Deprecated Attribute: The Deprecated attribute marks a class, method, property, class constants and functions that should not be used anymore
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Deprecated Attribute
	:og:type: article
	:og:description: The Deprecated attribute marks a class, method, property, class constants and functions that should not be used anymore
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Deprecated Attribute.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Attributes\/Deprecated.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Attributes\/Deprecated.html","name":"Deprecated Attribute","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"The Deprecated attribute marks a class, method, property, class constants and functions that should not be used anymore","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Deprecated Attribute.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The Deprecated `attribute <https://www.php.net/attribute>`_ marks a class, method, property, class constants and functions that should not be used anymore. The element is still usable in the current version, and it might be removed in a future version.

The full description of the deprecation include ``#[Deprecated(reason: '', replacement: '')]``. The reason parameter is a human readable reason for the change; the replacement parameter is a replacement suggestion. Only the `attribute <https://www.php.net/attribute>`_ is used in this rule.

.. code-block:: php
   
   <?php
   
   class x {
   	#[Deprecated]
   	function foo() {}
   }
   
   $x = new x;
   $x->foo();
   
   ?>

See also `#[Deprecated] <https://blog.jetbrains.com/phpstorm/2020/10/phpstorm-2020-3-eap-4/>`_.

Connex PHP features
-------------------

  + `Deprecation <https://php-dictionary.readthedocs.io/en/latest/dictionary/deprecation.ini.html>`_


Suggestions
___________

* Replace this call to another call, that is future proof.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Attributes/Deprecated                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Attributes <ruleset-Attributes>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


