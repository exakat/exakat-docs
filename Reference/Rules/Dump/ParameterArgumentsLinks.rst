.. _dump-parameterargumentslinks:

.. _links-between-parameter-and-argument:

Links Between Parameter And Argument
++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Links Between Parameter And Argument: Collect various stats about arguments and parameter usage.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Links Between Parameter And Argument
	:twitter:description: Links Between Parameter And Argument: Collect various stats about arguments and parameter usage
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Links Between Parameter And Argument
	:og:type: article
	:og:description: Collect various stats about arguments and parameter usage
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Links Between Parameter And Argument.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/ParameterArgumentsLinks.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/ParameterArgumentsLinks.html","name":"Links Between Parameter And Argument","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Collect various stats about arguments and parameter usage","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Links Between Parameter And Argument.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Collect various stats about arguments and parameter usage. 

A parameter is one slot in the method definition. An argument is a slot in the method call. Both are linked by the method and their respective position in the argument list.

+ Total number of argument usage, linked to a parameter : this excludes arguments from external libraries and native PHP functions. For reference.
+ Number of identical parameter : cases where argument and parameter have the same name. 
+ Number of different parameter : cases where argument and parameter have the different name. 
+ Number of expression argument : cases where argument is an expression
+ Number of constant argument : cases where the argument is a constant

.. code-block:: php
   
   <?php
   
   function foo($a, $b) {
       // some code
   }
   
   // $a is the same as the parameter
   // $c is different from the paramter $b
   foo($a, $c);
   
   const C = 1;
   
   // Foo is called with a constant (1rst argument)
   // Foo is called with a expression (2nd argument)
   foo(C, 1+3);
   
   ?>
Connex PHP features
-------------------

  + `parameter <https://php-dictionary.readthedocs.io/en/latest/dictionary/parameter.ini.html>`_
  + `argument <https://php-dictionary.readthedocs.io/en/latest/dictionary/argument.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/ParameterArgumentsLinks                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.6                                                                                                                                                                                   |
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


