.. _functions-noliteralforreference:


.. _no-literal-for-reference:

No Literal For Reference
++++++++++++++++++++++++

.. meta::
	:description:
		No Literal For Reference: Method arguments and return values may be by reference.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Literal For Reference
	:twitter:description: No Literal For Reference: Method arguments and return values may be by reference
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Literal For Reference
	:og:type: article
	:og:description: Method arguments and return values may be by reference
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Literal For Reference.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/NoLiteralForReference.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/NoLiteralForReference.html","name":"No Literal For Reference","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"Method arguments and return values may be by reference","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Literal For Reference.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Method arguments and return values may be by reference. Then, they need to be a valid variable.

Objects are always passed by reference, so there is no need to explicitly declare it.

Expressions, including ternary operator, produce value, and can't be used by reference directly. This is also the case for expression that include one or more reference. 

Wrongly passing a value as a reference leads to a PHP Notice.

.. code-block:: php
   
   <?php
   
   // variables, properties, static properties, array items are all possible
   $a = 1;
   foo($a);
   
   //This is not possible, as a literal can't be a reference
   foo(1);
   
   function foo(&$int) { return $int; }
   
   
   // This is not a valid reference
   function &bar() { return 2; }
   function &bar2() { return 2 + $r; }
   
   ?>

See also `References <https://www.php.net/references>`_.

Related PHP errors 
-------------------

  + `Cannot pass parameter %s by reference <https://php-errors.readthedocs.io/en/latest/messages/%25s%25s%25s%28%29%3A-argument-%23%25d%25s%25s%25s-must-be-passed-by-reference%2C-value-given.html>`_
  + `%s(): Argument #%s (%s) must be passed by reference, value given <https://php-errors.readthedocs.io/en/latest/messages/%25s%25s%25s%28%29%3A-argument-%23%25d%25s%25s%25s-must-be-passed-by-reference%2C-value-given.html>`_
  + `Only variable references should be returned by reference <https://php-errors.readthedocs.io/en/latest/messages/only-variable-references-should-be-returned-by-reference.html>`_



Connex PHP features
-------------------

  + `References <https://php-dictionary.readthedocs.io/en/latest/dictionary/reference.ini.html>`_
  + `Literal <https://php-dictionary.readthedocs.io/en/latest/dictionary/literal.ini.html>`_


Suggestions
___________

* Remove the reference in the method signature (argument or return value)
* Make the argument an object, by using a typehint (non-scalar)
* Put the value into a variable prior to call (or return) the method




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/NoLiteralForReference                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.5                                                                                                                                                                                   |
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


