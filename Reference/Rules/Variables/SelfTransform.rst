.. _variables-selftransform:

.. _self-transforming-variables:

Self-Transforming Variables
+++++++++++++++++++++++++++

.. meta::
	:description:
		Self-Transforming Variables: Variables that are assigned to themselves, after transformation.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Self-Transforming Variables
	:twitter:description: Self-Transforming Variables: Variables that are assigned to themselves, after transformation
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Self-Transforming Variables
	:og:type: article
	:og:description: Variables that are assigned to themselves, after transformation
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Self-Transforming Variables.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/SelfTransform.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/SelfTransform.html","name":"Self-Transforming Variables","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Variables that are assigned to themselves, after transformation","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Self-Transforming Variables.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Variables that are assigned to themselves, after transformation. Auto-transformations include appending element to an array, using post and pre increment operators, and assigning to the variable the `result <https://www.php.net/result>`_ of a call where the variable is also an argument.

.. code-block:: php
   
   <?php
   
   $s = strtolower($s);
   
   // filtering one element AND dropping all that not 1
   $a = array_filter('foo', $a[1]);
   
   $o->m = foo($o->m);
   
   ?>

Suggestions
___________

* Use new variables to hold transformed values.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/SelfTransform                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.0                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


