.. _structures-arrayaccessonliteralarray:


.. _array-access-on-literal-array:

Array Access On Literal Array
+++++++++++++++++++++++++++++


.. meta::

	:description:

		Array Access On Literal Array: Accessing an element on a literal array makes that array non-reusable.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Array Access On Literal Array

	:twitter:description: Array Access On Literal Array: Accessing an element on a literal array makes that array non-reusable

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Array Access On Literal Array

	:og:type: article

	:og:description: Accessing an element on a literal array makes that array non-reusable

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Array Access On Literal Array.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ArrayAccessOnLiteralArray.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ArrayAccessOnLiteralArray.html","name":"Array Access On Literal Array","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Accessing an element on a literal array makes that array non-reusable","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Array Access On Literal Array.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Accessing an element on a literal array makes that array non-reusable. 

It is recommended to make this array a constant or a property, for easier reusage. It also make that content more visiblem in the class definitions.

.. code-block:: php
   
   <?php
   
   class Suit {
   	const NAMES = ['Club' => 1, 'Spade' => 2, 'Heart' => 3, 'Diamond' => 4];
   
   	function __construct($name) {
   		if (!isset(self::NAMES[$name]) {
   			throw new Exception('Not a suit color');
   		}
   	}
   }
   
   class HiddenSuitList {
   	function __construct($name) {
   		if (!isset(['Club' => 1, 'Spade' => 2, 'Heart' => 3, 'Diamond' => 4][$name]) {
   			throw new Exception('Not a suit color');
   		}
   	}
   }
   
   ?>

Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ArrayAccessOnLiteralArray                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


