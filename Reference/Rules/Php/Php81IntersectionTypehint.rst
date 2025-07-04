.. _php-php81intersectiontypehint:


.. _intersection-type:

Intersection Type
+++++++++++++++++

.. meta::
	:description:
		Intersection Type: Intersection types allows the combination of several types for the same argument or return value.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Intersection Type
	:twitter:description: Intersection Type: Intersection types allows the combination of several types for the same argument or return value
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Intersection Type
	:og:type: article
	:og:description: Intersection types allows the combination of several types for the same argument or return value
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Intersection Type.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php81IntersectionTypehint.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php81IntersectionTypehint.html","name":"Intersection Type","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"Intersection types allows the combination of several types for the same argument or return value","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Intersection Type.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Intersection types allows the combination of several types for the same argument or return value. 

Several types are specified at the same place as a single one. The different values are separated by a ampersand character ``&``. 

Intersection types are a PHP 8.1 new feature.

.. code-block:: php
   
   <?php
   
   class Number {
       private A&B $object;
   }
   ?>

See also `PHP RFC: Pure intersection types <https://wiki.php.net/rfc/pure-intersection-types>`_, `Type declarations <https://www.php.net/manual/en/language.types.declarations.php>`_ and `How the New Intersection Types in PHP 8.1 Give You More Flexibility <https://www.cloudsavvyit.com/12907/how-the-new-intersection-types-in-php-8-1-give-you-more-flexibility/>`_.

Connex PHP features
-------------------

  + `Type System <https://php-dictionary.readthedocs.io/en/latest/dictionary/type.ini.html>`_
  + `Union Type <https://php-dictionary.readthedocs.io/en/latest/dictionary/union-type.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php81IntersectionTypehint                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


