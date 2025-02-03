.. _structures-implodeargsorder:


.. _implode()-arguments-order:

Implode() Arguments Order
+++++++++++++++++++++++++


.. meta::

	:description:

		Implode() Arguments Order: implode() used to accept two signatures, but is only recommending one.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Implode() Arguments Order

	:twitter:description: Implode() Arguments Order: implode() used to accept two signatures, but is only recommending one

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Implode() Arguments Order

	:og:type: article

	:og:description: implode() used to accept two signatures, but is only recommending one

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Implode() Arguments Order.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ImplodeArgsOrder.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ImplodeArgsOrder.html","name":"Implode() Arguments Order","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"implode() used to accept two signatures, but is only recommending one","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Implode() Arguments Order.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`implode() <https://www.php.net/implode>`_ used to accept two signatures, but is only recommending one. Both types orders of string then array, and array then string have been possible until PHP 7.4.

In PHP 7.4, the order array then string is deprecated, and emits a warning. It will be removed in PHP 8.0.

.. code-block:: php
   
   <?php
   
   $glue = ',';
   $pieces = range(0, 4);
   
   // documented argument order
   $s = implode($glue, $pieces);
   
   // Pre 7.4 argument order
   $s = implode($pieces, $glue);
   
   // both produces 0,1,2,3,4
   
   ?>

See also implode().


Suggestions
___________

* Always use the array as the second argument




Specs
_____

+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Structures/ImplodeArgsOrder                                                                                                                                                             |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 1.9.2                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                                                                                     |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                                                                         |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.4                                                                                                                                                                                 |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                               |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


