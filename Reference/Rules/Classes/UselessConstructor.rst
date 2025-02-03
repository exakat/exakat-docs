.. _classes-uselessconstructor:


.. _useless-constructor:

Useless Constructor
+++++++++++++++++++

.. meta::
	:description:
		Useless Constructor: Class constructor that have empty bodies are useless.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless Constructor
	:twitter:description: Useless Constructor: Class constructor that have empty bodies are useless
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless Constructor
	:og:type: article
	:og:description: Class constructor that have empty bodies are useless
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Useless Constructor.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UselessConstructor.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UselessConstructor.html","name":"Useless Constructor","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 21 Jan 2025 08:40:17 +0000","dateModified":"Tue, 21 Jan 2025 08:40:17 +0000","description":"Class constructor that have empty bodies are useless","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Useless Constructor.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Class constructor that have empty bodies are useless. They may be removed, as they are not called.

One edge case is when the class has a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_, and the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ constructor must not be called.

Another edge case is promoted properties: the body of the constructor is still empty, but the parameters hold the definitions of properties. These might be better outside the constructor though.


.. code-block:: php
   
   <?php
   
   class X {
       function __construct() {
           // Do nothing
       }
   }
   
   class Y extends X {
       // Useful constructor, as it prevents usage of the parent
       function __construct() {
           // Do nothing
       }
   }
   
   ?>
Related PHP errors 
-------------------

  + `Cannot call constructor <https://php-errors.readthedocs.io/en/latest/messages/cannot-call-constructor.html>`_



Connex PHP features
-------------------

  + `constructor <https://php-dictionary.readthedocs.io/en/latest/dictionary/constructor.ini.html>`_


Suggestions
___________

* Remove the constructor




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UselessConstructor                                                                                              |
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
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


