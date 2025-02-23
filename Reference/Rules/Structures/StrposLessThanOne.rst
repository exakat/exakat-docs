.. _structures-strposlessthanone:


.. _strpos()-less-than-one:

Strpos() Less Than One
++++++++++++++++++++++

.. meta::
	:description:
		Strpos() Less Than One: This rule reports a comparison of strpos() or stripos() with 1.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Strpos() Less Than One
	:twitter:description: Strpos() Less Than One: This rule reports a comparison of strpos() or stripos() with 1
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Strpos() Less Than One
	:og:type: article
	:og:description: This rule reports a comparison of strpos() or stripos() with 1
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Strpos() Less Than One.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/StrposLessThanOne.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/StrposLessThanOne.html","name":"Strpos() Less Than One","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This rule reports a comparison of strpos() or stripos() with 1","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Strpos() Less Than One.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports a comparison of `strpos() <https://www.php.net/strpos>`_ or `stripos() <https://www.php.net/stripos>`_ with 1. This is a variable of `strpos() <https://www.php.net/strpos>`_ == 0, since both `false <https://www.php.net/false>`_ and 0 are processed the same way. Yet, 0 might be a valid value.

This rule was suggested by Yann Ouche.


.. code-block:: php
   
   <?php
   
   // this works both when $a starts with .
   // and when the . is not in the string.
   if (strpos($a, '.') < 1) {
   
   }
   
   ?>

Suggestions
___________

* Make sure that the 2 cases are valid business cases.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/StrposLessThanOne                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Surprising <ruleset-Surprising>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.6                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+


