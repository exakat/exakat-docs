.. _complete-followclosuredefinition:


.. _follow-closure-definition:

Follow Closure Definition
+++++++++++++++++++++++++

.. meta::
	:description:
		Follow Closure Definition: This command adds DEFINITION link between closure and arrow functions definitions and their usage.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Follow Closure Definition
	:twitter:description: Follow Closure Definition: This command adds DEFINITION link between closure and arrow functions definitions and their usage
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Follow Closure Definition
	:og:type: article
	:og:description: This command adds DEFINITION link between closure and arrow functions definitions and their usage
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Follow Closure Definition.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/FollowClosureDefinition.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/FollowClosureDefinition.html","name":"Follow Closure Definition","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This command adds DEFINITION link between closure and arrow functions definitions and their usage","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Follow Closure Definition.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This command adds DEFINITION link between `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_ and arrow functions definitions and their usage.

Local usage of the `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_, in the same scope, are detected. Relayed `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_, when they are transmitted to another method for usage, is detected, for one jump.

This also supports first class callable, when the callable is defined in the code code (aka, not with native PHP functions or external libraries).

.. code-block:: php
   
   <?php
   
   function foo() {
       $closure = function () {};
       // Local usage
       echo $closure();
   }
   
   function bar(Closure $x) {
       // relayed usage
       echo $x(); 
   }
   
   
   ?>
Connex PHP features
-------------------

  + `Closure <https://php-dictionary.readthedocs.io/en/latest/dictionary/closure.ini.html>`_
  + `Arrow Functions <https://php-dictionary.readthedocs.io/en/latest/dictionary/arrow-function.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/FollowClosureDefinition                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


