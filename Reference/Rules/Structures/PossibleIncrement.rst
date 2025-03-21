.. _structures-possibleincrement:


.. _possible-increment:

Possible Increment
++++++++++++++++++

.. meta::
	:description:
		Possible Increment: This expression looks like a typo : a missing + would change the behavior.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Possible Increment
	:twitter:description: Possible Increment: This expression looks like a typo : a missing + would change the behavior
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Possible Increment
	:og:type: article
	:og:description: This expression looks like a typo : a missing + would change the behavior
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Possible Increment.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/PossibleIncrement.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/PossibleIncrement.html","name":"Possible Increment","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"This expression looks like a typo : a missing + would change the behavior","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Possible Increment.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This expression looks like a typo : a missing + would change the behavior.

The same pattern is not reported with -, as it is legit expression. + sign is usually understated, rather than explicit.

.. code-block:: php
   
   <?php
   
   // could it be a ++$b ? 
   $a = +$b;
   
   ?>

See also `Incrementing/Decrementing Operators <https://www.php.net/manual/en/language.operators.increment.php>`_ and `Arithmetic Operators <https://www.php.net/manual/en/language.operators.arithmetic.php>`_.

Connex PHP features
-------------------

  + `pre-increment <https://php-dictionary.readthedocs.io/en/latest/dictionary/pre-increment.ini.html>`_


Suggestions
___________

* Drop the whole assignation
* Complete the addition with another value : $a = 1 + $b
* Make this a ++ operator : ++$b
* Make this a negative operator : -$b
* Make the casting explicit : (int) $b




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/PossibleIncrement                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zurmo-structures-possibleincrement`, :ref:`case-mediawiki-structures-possibleincrement`                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


