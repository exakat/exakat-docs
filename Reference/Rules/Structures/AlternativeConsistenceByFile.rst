.. _structures-alternativeconsistencebyfile:


.. _alternative-syntax-consistence:

Alternative Syntax Consistence
++++++++++++++++++++++++++++++

.. meta::
	:description:
		Alternative Syntax Consistence: PHP allows for two syntax : the alternative syntax, and the classic syntax.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Alternative Syntax Consistence
	:twitter:description: Alternative Syntax Consistence: PHP allows for two syntax : the alternative syntax, and the classic syntax
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Alternative Syntax Consistence
	:og:type: article
	:og:description: PHP allows for two syntax : the alternative syntax, and the classic syntax
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Alternative Syntax Consistence.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/AlternativeConsistenceByFile.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/AlternativeConsistenceByFile.html","name":"Alternative Syntax Consistence","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"PHP allows for two syntax : the alternative syntax, and the classic syntax","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Alternative Syntax Consistence.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PHP allows for two syntax : the alternative syntax, and the classic syntax. 

The classic syntax is almost always used. When used, the alternative syntax is used in templates. 

This analysis reports files that are using both syntax at the same time. This is confusing.

.. code-block:: php
   
   <?php
   
   // Mixing both syntax is confusing.
   foreach($array as $item) : 
       if ($item > 1) {
           print "$item elementsn";
       } else {
           print "$item elementn";
       }
   endforeach;
   
   ?>
Connex PHP features
-------------------

  + `Alternative Syntax <https://php-dictionary.readthedocs.io/en/latest/dictionary/alternative-syntax.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/AlternativeConsistenceByFile                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.2                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


