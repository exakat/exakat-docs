.. _php-shortternary:

.. _short-ternary:

Short Ternary
+++++++++++++

.. meta::
	:description:
		Short Ternary: Short ternaries are the ternary operator, where the middle operand was left out.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Short Ternary
	:twitter:description: Short Ternary: Short ternaries are the ternary operator, where the middle operand was left out
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Short Ternary
	:og:type: article
	:og:description: Short ternaries are the ternary operator, where the middle operand was left out
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Short Ternary.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ShortTernary.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ShortTernary.html","name":"Short Ternary","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Short ternaries are the ternary operator, where the middle operand was left out","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Short Ternary.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Short ternaries are the ternary operator, where the middle operand was left out. 

Written that way, the operator checks if the first operand is empty() : in that case, the second operand is used; Otherwise, the first operand is used.

.. code-block:: php
   
   <?php
   	// $b is now 2
   	$b = $a ?: 2;
   	// $c is now 2 also 
   	$c = $b ?: 4;
   ?>

See also `Ternary Operator <https://www.php.net/manual/en/language.operators.comparison.php#language.operators.comparison.ternary>`_.

Connex PHP features
-------------------

  + `short-ternary <https://php-dictionary.readthedocs.io/en/latest/dictionary/short-ternary.ini.html>`_


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ShortTernary                                                                                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`One Liners <ruleset-One-Liners>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+


