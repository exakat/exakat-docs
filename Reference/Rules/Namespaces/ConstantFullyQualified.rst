.. _namespaces-constantfullyqualified:


.. _fully-qualified-constants:

Fully Qualified Constants
+++++++++++++++++++++++++

.. meta::
	:description:
		Fully Qualified Constants: Constants defined with their namespace.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Fully Qualified Constants
	:twitter:description: Fully Qualified Constants: Constants defined with their namespace
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Fully Qualified Constants
	:og:type: article
	:og:description: Constants defined with their namespace
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Fully Qualified Constants.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Namespaces\/ConstantFullyQualified.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Namespaces\/ConstantFullyQualified.html","name":"Fully Qualified Constants","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Constants defined with their namespace","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Fully Qualified Constants.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Constants defined with their namespace.

When defining constants with `define() <https://www.php.net/define>`_ function, it is possible to include the actual namespace : 
However, the name should be fully qualified without the initial \. Here, \a\b\c constant will never be accessible as a namespace constant, though it will be accessible via the `constant() <https://www.php.net/constant>`_ function.

Also, the namespace will be absolute, and not a relative namespace of the current one.

.. code-block:: php
   
   <?php
   
   define('a\b\c', 1); 
   
   ?>
Connex PHP features
-------------------

  + `Namespaces <https://php-dictionary.readthedocs.io/en/latest/dictionary/namespace.ini.html>`_


Suggestions
___________

* Drop the initial \ when creating constants with define() : for example, use trim($x, '\'), which removes anti-slashes before and after.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Namespaces/ConstantFullyQualified                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


