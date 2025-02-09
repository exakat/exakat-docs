.. _structures-emptywithexpression:


.. _empty-with-expression:

Empty With Expression
+++++++++++++++++++++

.. meta::
	:description:
		Empty With Expression: empty() doesn't accept expressions until PHP 5.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Empty With Expression
	:twitter:description: Empty With Expression: empty() doesn't accept expressions until PHP 5
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Empty With Expression
	:og:type: article
	:og:description: empty() doesn't accept expressions until PHP 5
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Empty With Expression.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/EmptyWithExpression.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/EmptyWithExpression.html","name":"Empty With Expression","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"empty() doesn't accept expressions until PHP 5","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Empty With Expression.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

empty() doesn't accept expressions until PHP 5.5. Until then, it is necessary to store the `result <https://www.php.net/result>`_ of the expression in a variable and then, test it with empty().

.. code-block:: php
   
   <?php
   
   // PHP 5.5+ empty() usage
   if (empty(strtolower($b . $c))) {
       doSomethingWithoutA();
   }
   
   // Compatible empty() usage
   $a = strtolower($b . $c);
   if (empty($a)) {
       doSomethingWithoutA();
   }
   
   ?>

See also `empty <http://www.php.net/empty>`_.

Connex PHP features
-------------------

  + `Empty <https://php-dictionary.readthedocs.io/en/latest/dictionary/empty.ini.html>`_


Suggestions
___________

* Use the compatible syntax, and store the result in a local variable before testing it with empty




Specs
_____

+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name       | Structures/EmptyWithExpression                                                                                          |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                   |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 5.5 and more recent                                                                                            |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity         | Major                                                                                                                   |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                         |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 5.5                                                                                                                 |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                               |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples         | :ref:`case-humo-gen-structures-emptywithexpression`                                                                     |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-------------------------------------------------------------------------------------------------------------------------+


