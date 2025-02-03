.. _structures-functionsubscripting:

.. _function-subscripting:

Function Subscripting
+++++++++++++++++++++

.. meta::
	:description:
		Function Subscripting: It is possible to use the result of a methodcall directly as an array, without storing the result in a temporary variable.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Function Subscripting
	:twitter:description: Function Subscripting: It is possible to use the result of a methodcall directly as an array, without storing the result in a temporary variable
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Function Subscripting
	:og:type: article
	:og:description: It is possible to use the result of a methodcall directly as an array, without storing the result in a temporary variable
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Function Subscripting.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/FunctionSubscripting.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/FunctionSubscripting.html","name":"Function Subscripting","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"It is possible to use the result of a methodcall directly as an array, without storing the result in a temporary variable","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Function Subscripting.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>It is possible to use the `result <https://www.php.net/result>`_ of a methodcall directly as an array, without storing the `result <https://www.php.net/result>`_ in a temporary variable.

This works, given that the method actually returns an array. 

This syntax was not possible until PHP 5.4. Until then, it was compulsory to store the `result <https://www.php.net/result>`_ in a variable first. Although this is now superfluous, it has been a standard syntax in PHP, and is still being used.
Storing the `result <https://www.php.net/result>`_ in a variable is still useful if the `result <https://www.php.net/result>`_ is actually used more than once.

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

See also `Accessing array elements with square bracket syntax <https://www.php.net/manual/en/language.types.array.php#language.types.array.syntax.accessing>`_.

Connex PHP features
-------------------

  + `subscripting <https://php-dictionary.readthedocs.io/en/latest/dictionary/subscripting.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/FunctionSubscripting                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.4 and more recent                                                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


