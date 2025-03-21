.. _traits-multipleusage:


.. _multiple-usage-of-same-trait:

Multiple Usage Of Same Trait
++++++++++++++++++++++++++++

.. meta::
	:description:
		Multiple Usage Of Same Trait: The same trait is used several times.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Multiple Usage Of Same Trait
	:twitter:description: Multiple Usage Of Same Trait: The same trait is used several times
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Multiple Usage Of Same Trait
	:og:type: article
	:og:description: The same trait is used several times
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Multiple Usage Of Same Trait.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Traits\/MultipleUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Traits\/MultipleUsage.html","name":"Multiple Usage Of Same Trait","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The same trait is used several times","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Multiple Usage Of Same Trait.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The same trait is used several times. One trait usage is sufficient.






PHP doesn't raise any `error <https://www.php.net/error>`_ when traits are included multiple times.

.. code-block:: php
   
   <?php
   
   // C is used twice, and could be dropped from B
   trait A { use B, C;}
   trait B { use C;}
   
   ?>

See also `Traits <https://www.php.net/manual/en/language.oop5.traits.php>`_.

Connex PHP features
-------------------

  + `Trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_


Suggestions
___________

* Remove any multiple traits from use expressions
* Review the class tree, and remove any trait mentioned multiple times




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/MultipleUsage                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-nextcloud-traits-multipleusage`                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


