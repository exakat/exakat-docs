.. _variables-php7indirectexpression:


.. _php-7-indirect-expression:

Php 7 Indirect Expression
+++++++++++++++++++++++++


.. meta::

	:description:

		Php 7 Indirect Expression: This rule reports variable indirect expressions, that are interpreted differently in PHP 5 and PHP 7.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Php 7 Indirect Expression

	:twitter:description: Php 7 Indirect Expression: This rule reports variable indirect expressions, that are interpreted differently in PHP 5 and PHP 7

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Php 7 Indirect Expression

	:og:type: article

	:og:description: This rule reports variable indirect expressions, that are interpreted differently in PHP 5 and PHP 7

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Php 7 Indirect Expression.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/Php7IndirectExpression.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/Php7IndirectExpression.html","name":"Php 7 Indirect Expression","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This rule reports variable indirect expressions, that are interpreted differently in PHP 5 and PHP 7","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Php 7 Indirect Expression.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports variable indirect expressions, that are interpreted differently in PHP 5 and PHP 7. 

They should be checked, as they will behave differently between these PHP versions.

.. code-block:: php
   
   <?php
   
   // Ambiguous expression : 
   $b = $$foo['bar']['baz'];
   echo $b;
   
   $foo = array('bar' => array('baz' => 'bat'));
   $bat = 'PHP 5.6';
   
   // In PHP 5, the expression above means : 
   $b = ${$foo['bar']['baz']};
   $b = 'PHP 5.6';
   
   $foo = 'a';
   $a = array('bar' => array('baz' => 'bat'));
   
   // In PHP 7, the expression above means : 
   $b = ($$foo)['bar']['baz'];
   $b = 'bat';
   
   ?>

See also `Changes to variable handling <https://www.php.net/manual/en/migration70.incompatible.php>`_.


Suggestions
___________

* Avoid using complex expressions, mixing $$, [0] and -> in the same expression
* Add curly braces {} to ensure that the precedence is the same between PHP 5 and 7. For example, ``$$v`` becomes ``${$v}``




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/Php7IndirectExpression                                                                                                                                                                                                                                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                                                                                                                                                                                                                                                                         |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


