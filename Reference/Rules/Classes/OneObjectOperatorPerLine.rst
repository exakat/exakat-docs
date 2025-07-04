.. _classes-oneobjectoperatorperline:


.. _one-object-operator-per-line:

One Object Operator Per Line
++++++++++++++++++++++++++++

.. meta::
	:description:
		One Object Operator Per Line: It is recommended to avoid using more than one operator -> per line, to prevent information overload.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: One Object Operator Per Line
	:twitter:description: One Object Operator Per Line: It is recommended to avoid using more than one operator -> per line, to prevent information overload
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: One Object Operator Per Line
	:og:type: article
	:og:description: It is recommended to avoid using more than one operator -> per line, to prevent information overload
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/One Object Operator Per Line.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/OneObjectOperatorPerLine.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/OneObjectOperatorPerLine.html","name":"One Object Operator Per Line","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 14 Jan 2025 12:52:58 +0000","dateModified":"Tue, 14 Jan 2025 12:52:58 +0000","description":"It is recommended to avoid using more than one operator -> per line, to prevent information overload","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/One Object Operator Per Line.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

It is recommended to avoid using more than one operator -> per line, to prevent information overload.

This rule applies to chained  calls, and not on distinct expressions, that may end up on the same line. 


.. code-block:: php
   
   <?php
   
   // Spread operators on multiple lines
   $object->firstMethodCall()
          ->property
          ->secondMethodCall();
   
   // This is not readable
   $object->firstMethodCall()->property->secondMethodCall();
   
   // This is OK, as objects are different.
   $a2->b2($c2->d2, $e2->f2); 
   
   ?>
Connex PHP features
-------------------

  + `Readability <https://php-dictionary.readthedocs.io/en/latest/dictionary/readability.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/OneObjectOperatorPerLine                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


