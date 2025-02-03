.. _namespaces-useduse:

.. _used-use:

Used Use
++++++++

.. meta::
	:description:
		Used Use: This rule lists the ``use`` statements.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Used Use
	:twitter:description: Used Use: This rule lists the ``use`` statements
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Used Use
	:og:type: article
	:og:description: This rule lists the ``use`` statements
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Used Use.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Namespaces\/UsedUse.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Namespaces\/UsedUse.html","name":"Used Use","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This rule lists the ``use`` statements","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Used Use.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>This rule lists the ``use`` statements. Those ``use`` are made to import namespaces structures, including functions and constants, and not to include traits in classes.

.. code-block:: php
   
   <?php
   
   namespace A {
       class b {}
   }
   
   namespace B {
       use A\B as B;
       
       new B();
   }
   
   ?>

See also `Using namespaces: Aliasing/Importing <https://www.php.net/manual/en/language.namespaces.importing.php>`_.

Connex PHP features
-------------------

  + `use <https://php-dictionary.readthedocs.io/en/latest/dictionary/use.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Namespaces/UsedUse                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


