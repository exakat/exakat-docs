.. _php-hasasymmetricvisibility:


.. _has-asymmetric-visibility:

Has Asymmetric Visibility
+++++++++++++++++++++++++

.. meta::
	:description:
		Has Asymmetric Visibility: This rule reports usage of asymmetric visibility in the source code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Has Asymmetric Visibility
	:twitter:description: Has Asymmetric Visibility: This rule reports usage of asymmetric visibility in the source code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Has Asymmetric Visibility
	:og:type: article
	:og:description: This rule reports usage of asymmetric visibility in the source code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Has Asymmetric Visibility.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/HasAsymmetricVisibility.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/HasAsymmetricVisibility.html","name":"Has Asymmetric Visibility","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 18 Feb 2025 18:21:43 +0000","dateModified":"Tue, 18 Feb 2025 18:21:43 +0000","description":"This rule reports usage of asymmetric visibility in the source code","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Has Asymmetric Visibility.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports usage of asymmetric visibility in the source code.

.. code-block:: php
   
   <?php
   
   class X {
       public private(set) int $property = 1;
   }
   
   ?>
Connex PHP features
-------------------

  + `Asymetric Visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/asymmetric-visibility.ini.html>`_


Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/HasAsymmetricVisibility                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CompatibilityPHP84 <ruleset-CompatibilityPHP84>`, :ref:`CompatibilityPHP85 <ruleset-CompatibilityPHP85>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.8                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.4 and more recent                                                                                                                                               |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


