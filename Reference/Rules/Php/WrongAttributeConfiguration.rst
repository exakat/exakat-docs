.. _php-wrongattributeconfiguration:


.. _wrong-attribute-configuration:

Wrong Attribute Configuration
+++++++++++++++++++++++++++++

.. meta::
	:description:
		Wrong Attribute Configuration: A class is attributed to the wrong PHP structure.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Wrong Attribute Configuration
	:twitter:description: Wrong Attribute Configuration: A class is attributed to the wrong PHP structure
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Wrong Attribute Configuration
	:og:type: article
	:og:description: A class is attributed to the wrong PHP structure
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Wrong Attribute Configuration.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/WrongAttributeConfiguration.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/WrongAttributeConfiguration.html","name":"Wrong Attribute Configuration","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"A class is attributed to the wrong PHP structure","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Wrong Attribute Configuration.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A class is attributed to the wrong PHP structure. A class may be an `attribute <https://www.php.net/attribute>`_, and it may also be configured to be used with different structures : classes, function, parameters, etc. When an `attribute <https://www.php.net/attribute>`_ has a configuration, it must be used with the correct structure.

.. code-block:: php
   
   <?php
   #[Attribute(Attribute::TARGET_CLASS)]
   class ClassAttribute { }
   
   // Wrong
   #[ClassAttribute]
   function foo () {}
   
   // OK
   #[ClassAttribute]
   class y  {}
   
   ?>

See also `Declaring Attribute Classes <https://www.php.net/manual/en/language.attributes.classes.php>`_.

Related PHP errors 
-------------------

  + `Attribute "AttributeFunction" cannot target Class (allowed targets: Function) <https://php-errors.readthedocs.io/en/latest/messages/attribute-%22%25s%22-cannot-target-%25s-%28allowed-targets%3A-%25s%29.html>`_



Connex PHP features
-------------------

  + `Attribute <https://php-dictionary.readthedocs.io/en/latest/dictionary/attribute.ini.html>`_


Suggestions
___________

* Remove the attribute from the wrongly attributed structure
* Extend the configuration of the attribute with Attribute::TARGET_*




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/WrongAttributeConfiguration                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


