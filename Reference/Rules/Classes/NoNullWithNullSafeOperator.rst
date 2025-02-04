.. _classes-nonullwithnullsafeoperator:


.. _no-null-with-null-safe-operator:

No Null With Null Safe Operator
+++++++++++++++++++++++++++++++

.. meta::
	:description:
		No Null With Null Safe Operator: When building an expression with a null-safe operator, it may fail and produce a NULL as a result.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Null With Null Safe Operator
	:twitter:description: No Null With Null Safe Operator: When building an expression with a null-safe operator, it may fail and produce a NULL as a result
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Null With Null Safe Operator
	:og:type: article
	:og:description: When building an expression with a null-safe operator, it may fail and produce a NULL as a result
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Null With Null Safe Operator.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/NoNullWithNullSafeOperator.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/NoNullWithNullSafeOperator.html","name":"No Null With Null Safe Operator","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"When building an expression with a null-safe operator, it may fail and produce a NULL as a result","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Null With Null Safe Operator.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When building an expression with a `null <https://www.php.net/`null <https://www.php.net/null>`_>`_-safe operator, it may fail and produce a `NULL <https://www.php.net/manual/en/language.types.`null <https://www.php.net/null>`_.php>`_ as a `result <https://www.php.net/result>`_. When the last method of the expression also returns `null <https://www.php.net/`null <https://www.php.net/null>`_>`_ (or void, which is transformed in `null) <https://www.php.net/`null <https://www.php.net/null>`_>`_, then it is not possible to differentiate between a failure and a valid execution of the method. 

As such, it is recommended to avoid finishing with a method that returns `null <https://www.php.net/`null <https://www.php.net/null>`_>`_, in an expression that uses a `null <https://www.php.net/`null <https://www.php.net/null>`_>`_-safe operator.

.. code-block:: php
   
   <?php
   
   class x {
   	function foo($a) : ?int { 
   		if ($a % 2) {
   			return $a;
   		} else {
   			return null;
   		}
   	}
   }
   
   $x = x::getInstance(x::class);
   $result = $x?->foo($a);
   
   // Is that an error or a valid result ? 
   if ($result === null) { }
   
   ?>
Connex PHP features
-------------------

  + `Null Safe Object Operator <https://php-dictionary.readthedocs.io/en/latest/dictionary/nullsafe-object-operator.ini.html>`_


Suggestions
___________

* Avoid using the null-safe operator in that expression
* Make the last property / method in the expression not return null




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/NoNullWithNullSafeOperator                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | 8.1                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


