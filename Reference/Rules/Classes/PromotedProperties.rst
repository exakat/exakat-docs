.. _classes-promotedproperties:

.. _promoted-properties:

Promoted Properties
+++++++++++++++++++

.. meta::
	:description:
		Promoted Properties: Promoted properties is a way to declare the properties within the constructor, and have them assigned to the constructing value at instantiation.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Promoted Properties
	:twitter:description: Promoted Properties: Promoted properties is a way to declare the properties within the constructor, and have them assigned to the constructing value at instantiation
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Promoted Properties
	:og:type: article
	:og:description: Promoted properties is a way to declare the properties within the constructor, and have them assigned to the constructing value at instantiation
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Promoted Properties.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/PromotedProperties.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/PromotedProperties.html","name":"Promoted Properties","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Promoted properties is a way to declare the properties within the constructor, and have them assigned to the constructing value at instantiation","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Promoted Properties.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Promoted properties is a way to declare the properties within the constructor, and have them assigned to the constructing value at instantiation.

.. code-block:: php
   
   <?php
   
       class CustomerDTO
       {
           public function __construct(
               public string $name, 
               public string $email, 
               public DateTimeImmutable $birth_date,
           ) {}
       }
       
   ?>

See also `Constructor Promotion <https://www.php.net/manual/en/language.oop5.decon.php#language.oop5.decon.constructor.promotion>`_ and `PHP 8: Constructor property promotion <https://stitcher.io/blog/constructor-promotion-in-php-8>`_.

Connex PHP features
-------------------

  + `promoted-property <https://php-dictionary.readthedocs.io/en/latest/dictionary/promoted-property.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/PromotedProperties                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Inventory <ruleset-Inventory>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.1                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


