.. _structures-uselesscheck:


.. _useless-check:

Useless Check
+++++++++++++

.. meta::
	:description:
		Useless Check: There is no need to check the size of an array content before using foreach.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless Check
	:twitter:description: Useless Check: There is no need to check the size of an array content before using foreach
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless Check
	:og:type: article
	:og:description: There is no need to check the size of an array content before using foreach
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Useless Check.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UselessCheck.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UselessCheck.html","name":"Useless Check","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"There is no need to check the size of an array content before using foreach","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Useless Check.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

There is no need to check the size of an array content before using foreach. `Foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ applies a test on the source, and skips the loop if no element is found.

This analysis checks for conditions with `sizeof() <https://www.php.net/sizeof>`_ and `count() <https://www.php.net/count>`_. Conditions with `isset() <https://www.www.php.net/isset>`_ and empty() are omitted : they also check for the variable existence, and thus, offer extra coverage.

.. code-block:: php
   
   <?php
   
   // Checking for type is good. 
   if (is_array($array)) {
       foreach($array as $a) {
           doSomething($a);
       }
   }
   
   // Foreach on empty arrays doesn't start. Checking is useless
   if (!empty($array)) {
       foreach($array as $a) {
           doSomething($a);
       }
   }
   
   ?>

See also `foreach <https://www.php.net/manual/en/control-structures.foreach.php>`_.

Connex PHP features
-------------------

  + `Validation <https://php-dictionary.readthedocs.io/en/latest/dictionary/validation.ini.html>`_


Suggestions
___________

* Drop the condition and the check
* Turn the condition into isset(), empty() and is_array()




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UselessCheck                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.9                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-magento-structures-uselesscheck`, :ref:`case-phinx-structures-uselesscheck`                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


