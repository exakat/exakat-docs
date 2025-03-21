.. _php-mixedkeyword:


.. _the-mixed-keyword:

The Mixed Keyword
+++++++++++++++++

.. meta::
	:description:
		The Mixed Keyword: `mixed` has becomes a PHP keyword.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: The Mixed Keyword
	:twitter:description: The Mixed Keyword: `mixed` has becomes a PHP keyword
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: The Mixed Keyword
	:og:type: article
	:og:description: `mixed` has becomes a PHP keyword
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/The Mixed Keyword.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/MixedKeyword.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/MixedKeyword.html","name":"The Mixed Keyword","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"`mixed` has becomes a PHP keyword","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/The Mixed Keyword.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`mixed` has becomes a PHP keyword. It is used for explicitly typing methods, argument or properties which accept any type of data.

That name should be avoided in classes, traits, enumerations and interfaces. Methods, anonymous classes (sic), namespaces and functions are OK to use it. 


.. code-block:: php
   
   <?php
   
   // This is OK
   function mixed() { } 
   
   // This is not possible anymore in PHP 8.0.
   class mixed {  } 
   
   ?>

See also `mixed <hhttps://www.php.net/manual/en/language.types.declarations.php#language.types.declarations.mixed>`_.

Related PHP errors 
-------------------

  + `Cannot use 'mixed' as class name as it is reserved <https://php-errors.readthedocs.io/en/latest/messages/cannot-use-%27mixed%27-as-class-name-as-it-is-reserved.html>`_



Connex PHP features
-------------------

  + `Mixed <https://php-dictionary.readthedocs.io/en/latest/dictionary/mixed.ini.html>`_


Suggestions
___________

* Rename the classes, traits and interfaces with a different name.




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/MixedKeyword                                                                                                                                                                             |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.0                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


