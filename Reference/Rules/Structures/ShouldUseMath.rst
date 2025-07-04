.. _structures-shouldusemath:


.. _should-use-math:

Should Use Math
+++++++++++++++

.. meta::
	:description:
		Should Use Math: Use math operators to make the operation readable.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Should Use Math
	:twitter:description: Should Use Math: Use math operators to make the operation readable
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Should Use Math
	:og:type: article
	:og:description: Use math operators to make the operation readable
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Should Use Math.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ShouldUseMath.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ShouldUseMath.html","name":"Should Use Math","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Use math operators to make the operation readable","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Should Use Math.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Use math operators to make the operation readable.

.. code-block:: php
   
   <?php
   
   // Adding one to self
   $a *= 2;
   // same as above
   $a += $a;
   
   // Squaring oneself
   $a \*\*\= 2;
   // same as above
   $a *= $a;
   
   // Removing oneself
   $a = 0;
   // same as above
   $a -= $a;
   
   // Dividing oneself
   $a = 1;
   // same as above
   $a /= $a;
   
   // Divisition remainer
   $a = 0;
   // same as above
   $a %= $a;
   
   ?>

See also `Mathematical Functions <https://www.php.net/manual/en/book.math.php>`_.


Suggestions
___________

* Use explicit math assignation




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ShouldUseMath                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-openemr-structures-shouldusemath`                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


