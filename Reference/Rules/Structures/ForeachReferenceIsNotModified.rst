.. _structures-foreachreferenceisnotmodified:


.. _foreach-reference-is-not-modified:

Foreach Reference Is Not Modified
+++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Foreach Reference Is Not Modified: Foreach statement may loop using a reference, especially when the loop has to change values of the array it is looping on.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Foreach Reference Is Not Modified
	:twitter:description: Foreach Reference Is Not Modified: Foreach statement may loop using a reference, especially when the loop has to change values of the array it is looping on
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Foreach Reference Is Not Modified
	:og:type: article
	:og:description: Foreach statement may loop using a reference, especially when the loop has to change values of the array it is looping on
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Foreach Reference Is Not Modified.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ForeachReferenceIsNotModified.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ForeachReferenceIsNotModified.html","name":"Foreach Reference Is Not Modified","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Foreach statement may loop using a reference, especially when the loop has to change values of the array it is looping on","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Foreach Reference Is Not Modified.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Foreach statement may loop using a reference, especially when the loop has to change values of the array it is looping on. 

In the spotted loop, reference are used but never modified. They may be removed.

.. code-block:: php
   
   <?php
   
   $letters = range('a', 'z');
   
   // $letter is not used here
   foreach($letters as &$letter) {
       $alphabet .= $letter;
   }
   
   // $letter is actually used here
   foreach($letters as &$letter) {
       $letter = strtoupper($letter);
   }
   
   ?>
Connex PHP features
-------------------

  + `Foreach <https://php-dictionary.readthedocs.io/en/latest/dictionary/foreach.ini.html>`_
  + `References <https://php-dictionary.readthedocs.io/en/latest/dictionary/reference.ini.html>`_


Suggestions
___________

* Remove the reference from the foreach
* Actually modify the content of the reference




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ForeachReferenceIsNotModified                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolibarr-structures-foreachreferenceisnotmodified`, :ref:`case-vanilla-structures-foreachreferenceisnotmodified`                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


