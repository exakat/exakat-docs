.. _functions-recursive:


.. _recursive-functions:

Recursive Functions
+++++++++++++++++++

.. meta::
	:description:
		Recursive Functions: Recursive methods are methods that calls itself.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Recursive Functions
	:twitter:description: Recursive Functions: Recursive methods are methods that calls itself
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Recursive Functions
	:og:type: article
	:og:description: Recursive methods are methods that calls itself
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Recursive Functions.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/Recursive.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/Recursive.html","name":"Recursive Functions","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Recursive methods are methods that calls itself","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Recursive Functions.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Recursive methods are methods that calls itself. 

Usually, the method call itself directly. In rarer occasions, the method calls another method which calls it back; such cycle are longer and not detected here.



Functions, methods, arrow functions and closures are identified as recursive. Higher level of recursion are not detected (function a() calls function b(), calls function a(), etc.).

Functions are easy to identify as recursive. Methods have some blind spots : when the injected argument is of the same class, it may lead to recursion too. On the other hand, calling the same method on a property is not sufficient, as the property might not be ``$this``.

.. code-block:: php
   
   <?php
   
   // a recursive function ; it calls itself
   function factorial($n) {
       if ($n == 1) { return 1; }
       
       return factorial($n - 1) * $n;
   }
   ?>
Connex PHP features
-------------------

  + `Recursion <https://php-dictionary.readthedocs.io/en/latest/dictionary/recursion.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/Recursive                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


