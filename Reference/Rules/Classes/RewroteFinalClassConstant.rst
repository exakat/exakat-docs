.. _classes-rewrotefinalclassconstant:


.. _rewrote-final-class-constant:

Rewrote Final Class Constant
++++++++++++++++++++++++++++

.. meta::
	:description:
		Rewrote Final Class Constant: Final class constants can't be rewriten in a child class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Rewrote Final Class Constant
	:twitter:description: Rewrote Final Class Constant: Final class constants can't be rewriten in a child class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Rewrote Final Class Constant
	:og:type: article
	:og:description: Final class constants can't be rewriten in a child class
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Rewrote Final Class Constant.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/RewroteFinalClassConstant.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/RewroteFinalClassConstant.html","name":"Rewrote Final Class Constant","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"Final class constants can't be rewriten in a child class","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Rewrote Final Class Constant.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Final class constants can't be rewriten in a child class. 

It is possible to write code that lints, when the classes are in different files. Such overwrites will only be detected at execution time.

.. code-block:: php
   
   <?php
   
   class x {
   	final const A = 1;
   	const B = 1;
   }
   
   class y extends x {
   	const A = 1;
   	const B = 1;
   }
   
   ?>
Related PHP errors 
-------------------

  + `Cannot override final constant %s::%s <https://php-errors.readthedocs.io/en/latest/messages/%25s%3A%3A%25s-cannot-override-final-constant-%25s%3A%3A%25s.html>`_



Connex PHP features
-------------------

  + `Final Keyword <https://php-dictionary.readthedocs.io/en/latest/dictionary/final.ini.html>`_


Suggestions
___________

* Remove the final keyword
* Remove the rewritten constant




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/RewroteFinalClassConstant                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.4                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


