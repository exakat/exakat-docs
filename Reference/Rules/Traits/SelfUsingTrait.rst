.. _traits-selfusingtrait:


.. _self-using-trait:

Self Using Trait
++++++++++++++++

.. meta::
	:description:
		Self Using Trait: Trait uses itself : this is unnecessary.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Self Using Trait
	:twitter:description: Self Using Trait: Trait uses itself : this is unnecessary
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Self Using Trait
	:og:type: article
	:og:description: Trait uses itself : this is unnecessary
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Self Using Trait.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Traits\/SelfUsingTrait.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Traits\/SelfUsingTrait.html","name":"Self Using Trait","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Trait uses itself : this is unnecessary","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Self Using Trait.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Trait uses itself : this is unnecessary. Traits may use themselves, or be used by other traits, that are using the initial trait itself. 

PHP handles the situation quietly, by ignoring all extra use of the same trait, keeping only one valid version.

.. code-block:: php
   
   <?php
   
   // empty, but valid
   trait a {} 
   
   // obvious self usage
   trait b { use b; }
   
   // less obvious self usage
   trait c { use d, e, f, g, h, c; }
   
   // level 2 self usage
   trait i { use j; }
   trait j { use i; }
   
   ?>

See also `Traits <https://www.php.net/manual/en/language.oop5.traits.php>`_.

Connex PHP features
-------------------

  + `trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_


Suggestions
___________

* Remove the extra usage of the trait.




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/SelfUsingTrait                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`Dead code <ruleset-Dead-code>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.7                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                           |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+


