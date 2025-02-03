.. _classes-mutualextension:

.. _classes-mutually-extending-each-other:

Classes Mutually Extending Each Other
+++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Classes Mutually Extending Each Other: Those classes are extending each other, creating an extension loop.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Classes Mutually Extending Each Other
	:twitter:description: Classes Mutually Extending Each Other: Those classes are extending each other, creating an extension loop
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Classes Mutually Extending Each Other
	:og:type: article
	:og:description: Those classes are extending each other, creating an extension loop
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Classes Mutually Extending Each Other.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/MutualExtension.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/MutualExtension.html","name":"Classes Mutually Extending Each Other","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Those classes are extending each other, creating an extension loop","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Classes Mutually Extending Each Other.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Those classes are extending each other, creating an extension loop. PHP will yield a fatal `error <https://www.php.net/error>`_ at running time, even if it is compiling the code.

.. code-block:: php
   
   <?php
   
   // This code is lintable but won't run
   class Foo extends Bar { }
   class Bar extends Foo { }
   
   // The loop may be quite large
   class Foo extends Bar { }
   class Bar extends Bar2 { }
   class Bar2 extends Foo { }
   
   ?>
Connex PHP features
-------------------

  + `extends <https://php-dictionary.readthedocs.io/en/latest/dictionary/extends.ini.html>`_


Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MutualExtension                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


