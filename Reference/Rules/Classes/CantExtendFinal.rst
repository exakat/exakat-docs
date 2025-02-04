.. _classes-cantextendfinal:


.. _can't-extend-final-class:

Can't Extend Final Class
++++++++++++++++++++++++

.. meta::
	:description:
		Can't Extend Final Class: It is not possible to extend final classes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Can't Extend Final Class
	:twitter:description: Can't Extend Final Class: It is not possible to extend final classes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Can't Extend Final Class
	:og:type: article
	:og:description: It is not possible to extend final classes
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Can't Extend Final Class.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CantExtendFinal.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CantExtendFinal.html","name":"Can't Extend Final Class","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 21 Jan 2025 08:40:17 +0000","dateModified":"Tue, 21 Jan 2025 08:40:17 +0000","description":"It is not possible to extend final classes","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Can't Extend Final Class.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

It is not possible to extend final classes. 

Since PHP fails with a fatal `error <https://www.php.net/error>`_, this means that the extending class is probably not used in the rest of the code. Check for dead code.

In a separate file :

.. code-block:: php
   
   <?php
       // File Foo
       final class foo {
           public final function bar() {
               // doSomething
           }
       }
   ?>

See also `Final Keyword <https://www.php.net/manual/en/language.oop5.final.php>`_.

Related PHP errors 
-------------------

  + `Class %s cannot extend final class %s <https://php-errors.readthedocs.io/en/latest/messages/class-%25s-cannot-extend-%25s-%25s.html>`_



Connex PHP features
-------------------

  + `Final Keyword <https://php-dictionary.readthedocs.io/en/latest/dictionary/final.ini.html>`_


Suggestions
___________

* Remove the final keyword
* Remove the extending class




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CantExtendFinal                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


