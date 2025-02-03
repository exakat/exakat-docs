.. _interfaces-uselessinterfaces:

.. _useless-interfaces:

Useless Interfaces
++++++++++++++++++

.. meta::
	:description:
		Useless Interfaces: The interfaces below are defined and are implemented by some classes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless Interfaces
	:twitter:description: Useless Interfaces: The interfaces below are defined and are implemented by some classes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless Interfaces
	:og:type: article
	:og:description: The interfaces below are defined and are implemented by some classes
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Useless Interfaces.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Interfaces\/UselessInterfaces.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Interfaces\/UselessInterfaces.html","name":"Useless Interfaces","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The interfaces below are defined and are implemented by some classes","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Useless Interfaces.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>The interfaces below are defined and are implemented by some classes. 

However, they are never used to enforce an object's class in the code, using ``instanceof`` or in a type. 
As they are currently used, those interfaces may be removed without change in behavior.
Interfaces should be used in type or with the ``instanceof`` operator.

.. code-block:: php
   
   <?php
       // only defined interface but never enforced
       interface i {};
       class c implements i {} 
   ?>
Connex PHP features
-------------------

  + `interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/interface.ini.html>`_


Suggestions
___________

* Use the interface with instanceof, or a type
* Drop the interface altogether : both definition and implements keyword




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/UselessInterfaces                                                                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`Typechecks <ruleset-Typechecks>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-useless-interfaces <https://github.com/dseguy/clearPHP/tree/master/rules/no-useless-interfaces.md>`__                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-woocommerce-interfaces-uselessinterfaces`                                                                                                                                               |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


