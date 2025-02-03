.. _structures-unsupportedoperandtypes:


.. _unsupported-operand-types:

Unsupported Operand Types
+++++++++++++++++++++++++

.. meta::
	:description:
		Unsupported Operand Types: This error is raised when trying to combine two values of incompatible type.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unsupported Operand Types
	:twitter:description: Unsupported Operand Types: This error is raised when trying to combine two values of incompatible type
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unsupported Operand Types
	:og:type: article
	:og:description: This error is raised when trying to combine two values of incompatible type
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unsupported Operand Types.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UnsupportedOperandTypes.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UnsupportedOperandTypes.html","name":"Unsupported Operand Types","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 16 Jan 2025 17:40:16 +0000","dateModified":"Thu, 16 Jan 2025 17:40:16 +0000","description":"This error is raised when trying to combine two values of incompatible type","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unsupported Operand Types.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This `error <https://www.php.net/error>`_ is raised when trying to combine two values of incompatible type. For example, adding an array and an integer; adding an integer with an object; etc.

Always checks that the types are compatible with the planned operations.

That compatibility may be tricky with numeric strings: these are string that PHP can easily convert to an integer or a float. In such case, they are considered as their converted values.

PHP detects this `error <https://www.php.net/error>`_ at linting time, when using literal values. When `static <https://www.php.net/manual/en/language.oop5.static.php>`_ or dynamic expression are involved, this `error <https://www.php.net/error>`_ appears at execution time.

.. code-block:: php
   
   <?php
   
   const MY_ARRAY = 'error';
   
   // Unsupported operand types
   $b = MY_ARRAY + array(3,4);
   
   ?>

See also `PHP - Fatal error: Unsupported operand types [duplicate] <https://stackoverflow.com/questions/2108875/php-fatal-error-unsupported-operand-types>`_.

Related PHP errors 
-------------------

  + `Unsupported operand types <https://php-errors.readthedocs.io/en/latest/messages/unsupported-operand-types.html>`_



Connex PHP features
-------------------

  + `plus <https://php-dictionary.readthedocs.io/en/latest/dictionary/plus.ini.html>`_


Suggestions
___________

* Make sure all the planned operations are compatible with the type used.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UnsupportedOperandTypes                                                                                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.2                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


