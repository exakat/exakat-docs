.. _structures-functionpresubscripting:


.. _function-subscripting,-old-style:

Function Subscripting, Old Style
++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Function Subscripting, Old Style: It is possible use function results as an array, and read directly its element.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Function Subscripting, Old Style
	:twitter:description: Function Subscripting, Old Style: It is possible use function results as an array, and read directly its element
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Function Subscripting, Old Style
	:og:type: article
	:og:description: It is possible use function results as an array, and read directly its element
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Function Subscripting, Old Style.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/FunctionPreSubscripting.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/FunctionPreSubscripting.html","name":"Function Subscripting, Old Style","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"It is possible use function results as an array, and read directly its element","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Function Subscripting, Old Style.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

It is possible use function results as an array, and read directly its element. This was added in PHP 5.4.

.. code-block:: php
   
   <?php
   
   function foo() {
       return array(1 => 'a', 'b', 'c');
   }
   
   echo foo()[1]; // displays 'a';
   
   // Function subscripting, the old way
   function foo() {
       return array(1 => 'a', 'b', 'c');
   }
   
   $x = foo();
   echo $x[1]; // displays 'a';
   
   ?>
Connex PHP features
-------------------

  + `Function Subscripting <https://php-dictionary.readthedocs.io/en/latest/dictionary/function-subscripting.ini.html>`_


Suggestions
___________

* Skip the local variable and directly use the return value from the function




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/FunctionPreSubscripting                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.4 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-openconf-structures-functionpresubscripting`                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


