.. _classes-uselessfinal:


.. _useless-final:

Useless Final
+++++++++++++

.. meta::
	:description:
		Useless Final: When a class is declared final, all of its methods are also final by default.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless Final
	:twitter:description: Useless Final: When a class is declared final, all of its methods are also final by default
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless Final
	:og:type: article
	:og:description: When a class is declared final, all of its methods are also final by default
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Useless Final.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UselessFinal.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UselessFinal.html","name":"Useless Final","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"When a class is declared final, all of its methods are also final by default","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Useless Final.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When a class is declared final, all of its methods are also final by default. 

There is no need to declare them individually final.

.. code-block:: php
   
   <?php
   
       final class foo {
           // Useless final, as the whole class is final
           final function method() { }
       }
   
       class bar {
           // Useful final, as the whole class is not final
           final function method() { }
       }
   
   ?>

See also `Final Keyword <https://www.php.net/manual/en/language.oop5.final.php>`_ and `When to declare final <https://ocramius.github.io/blog/when-to-declare-classes-final/>`_.

Connex PHP features
-------------------

  + `Final Keyword <https://php-dictionary.readthedocs.io/en/latest/dictionary/final.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UselessFinal                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-useless-final <https://github.com/dseguy/clearPHP/tree/master/rules/no-useless-final.md>`__                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


