.. _complete-overwrittenmethods:


.. _overwritten-methods:

Overwritten Methods
+++++++++++++++++++

.. meta::
	:description:
		Overwritten Methods: This command adds OVERWRITE link between methods definitions of classes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Overwritten Methods
	:twitter:description: Overwritten Methods: This command adds OVERWRITE link between methods definitions of classes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Overwritten Methods
	:og:type: article
	:og:description: This command adds OVERWRITE link between methods definitions of classes
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Overwritten Methods.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/OverwrittenMethods.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/OverwrittenMethods.html","name":"Overwritten Methods","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This command adds OVERWRITE link between methods definitions of classes","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Overwritten Methods.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This command adds OVERWRITE link between methods definitions of classes.

The `foo` method will be linked between classes x and y, with an OVERWRITE link.

.. code-block:: php
   
   <?php
   
   class X {
       protected function foo() {}
   }
   
   class Y extends X {
       protected function foo() {}
   }
   
   ?>
Connex PHP features
-------------------

  + `Class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `Inheritance <https://php-dictionary.readthedocs.io/en/latest/dictionary/inheritance.ini.html>`_
  + `Method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/OverwrittenMethods                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`NoDoc <ruleset-NoDoc>`                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


