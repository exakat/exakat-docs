.. _arrays-randomlysortedliterals:

.. _randomly-sorted-arrays:

Randomly Sorted Arrays
++++++++++++++++++++++

.. meta::
	:description:
		Randomly Sorted Arrays: Those literal arrays are written in several places, but their items are in various orders.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Randomly Sorted Arrays
	:twitter:description: Randomly Sorted Arrays: Those literal arrays are written in several places, but their items are in various orders
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Randomly Sorted Arrays
	:og:type: article
	:og:description: Those literal arrays are written in several places, but their items are in various orders
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Randomly Sorted Arrays.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Arrays\/RandomlySortedLiterals.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Arrays\/RandomlySortedLiterals.html","name":"Randomly Sorted Arrays","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Those literal arrays are written in several places, but their items are in various orders","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Randomly Sorted Arrays.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Those literal arrays are written in several places, but their items are in various orders. 

This may reduce the reading and proofing of the arrays, and induce confusion. The random order may also be a residue of development : both arrays started with different values, but they grew overtime to handle the same items. The way they were written lead to the current order.

Unless order is important, it is recommended to always use the same order when defining literal arrays. This makes it easier to match different part of the code by recognizing one of its literal.

.. code-block:: php
   
   <?php
   
   // an array
   $set = [1,3,5,9,10];
   
   function foo() {
       // an array, with the same values but different order, in a different context
       $list = [1,3,5,10,9,];
   }
   
   // an array, with the same order than the initial one
   $inits = [1,3,5,9,10];
   
   ?>

+---------+---------+---------+-----------------------------------+
| Name    | Default | Type    | Description                       |
+---------+---------+---------+-----------------------------------+
| maxSize | 5       | integer | Maximal size of arrays to survey. |
+---------+---------+---------+-----------------------------------+


Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Suggestions
___________

* Match the sorting order of the arrays. Choose any of them.
* Configure a constant and use it as a replacement for those arrays.
* Leave the arrays intact : the order may be important.
* For hash arrays, consider turning the array in a class.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/RandomlySortedLiterals                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Suggestions <ruleset-Suggestions>`                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.2                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-contao-arrays-randomlysortedliterals`, :ref:`case-vanilla-arrays-randomlysortedliterals`                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


