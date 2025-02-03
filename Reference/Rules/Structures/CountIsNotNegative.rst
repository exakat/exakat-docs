.. _structures-countisnotnegative:


.. _count()-is-not-negative:

Count() Is Not Negative
+++++++++++++++++++++++

.. meta::
	:description:
		Count() Is Not Negative: This rule reports when the Countable method ``count`` is poised to return a negative value.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Count() Is Not Negative
	:twitter:description: Count() Is Not Negative: This rule reports when the Countable method ``count`` is poised to return a negative value
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Count() Is Not Negative
	:og:type: article
	:og:description: This rule reports when the Countable method ``count`` is poised to return a negative value
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Count() Is Not Negative.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CountIsNotNegative.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CountIsNotNegative.html","name":"Count() Is Not Negative","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"This rule reports when the Countable method ``count`` is poised to return a negative value","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Count() Is Not Negative.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports when the `Countable <https://www.php.net/countable>`_ method ``count`` is poised to return a negative value. 

It also reports when a call to ``count()`` is compared to a value that might be negative.

.. code-block:: php
   
   <?php
   
   // count() shall not be below 0, so === is preferable here
   if (count($array) <= 0) { }
   
   ?>
Connex PHP features
-------------------

  + `count <https://php-dictionary.readthedocs.io/en/latest/dictionary/count.ini.html>`_
  + `negative <https://php-dictionary.readthedocs.io/en/latest/dictionary/negative.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CountIsNotNegative                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


