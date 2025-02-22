.. _php-couldusepromotedproperties:


.. _could-use-promoted-properties:

Could Use Promoted Properties
+++++++++++++++++++++++++++++

.. meta::
	:description:
		Could Use Promoted Properties: Promoted properties are a syntax notation where the properties are declared as arguments of the constructor.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Use Promoted Properties
	:twitter:description: Could Use Promoted Properties: Promoted properties are a syntax notation where the properties are declared as arguments of the constructor
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Use Promoted Properties
	:og:type: article
	:og:description: Promoted properties are a syntax notation where the properties are declared as arguments of the constructor
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Use Promoted Properties.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/CouldUsePromotedProperties.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/CouldUsePromotedProperties.html","name":"Could Use Promoted Properties","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Promoted properties are a syntax notation where the properties are declared as arguments of the constructor","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Use Promoted Properties.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Promoted properties are a syntax notation where the properties are declared as arguments of the constructor. 

They reduce PHP code at `__construct() <https://www.php.net/manual/en/language.oop5.decon.php>`_ time. This feature is available in PHP 8.0.

.. code-block:: php
   
   <?php
   
   class x {
       function __construct($a, $b) {
           // $a argument may be promoted to property $c
           $this->c = $a;
           
           // $b argument cannot be upgraded to property, as it is updated. 
           // Move the addition to the new call, or keep the syntax below
           $this->d = $b + 2;
       }
   }
   
   ?>

See also `PHP 8: Constructor property promotion <https://stitcher.io/blog/constructor-promotion-in-php-8>`_ and `PHP RFC: Constructor Property Promotion <https://wiki.php.net/rfc/constructor_promotion>`_.

Connex PHP features
-------------------

  + `Promoted Properties <https://php-dictionary.readthedocs.io/en/latest/dictionary/promoted-property.ini.html>`_


Suggestions
___________

* Update the constructor syntax, and remove the property specification.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/CouldUsePromotedProperties                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.9                                                                                                                   |
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


