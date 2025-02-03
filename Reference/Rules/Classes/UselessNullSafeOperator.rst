.. _classes-uselessnullsafeoperator:


.. _useless-nullsafe-operator:

Useless NullSafe Operator
+++++++++++++++++++++++++

.. meta::
	:description:
		Useless NullSafe Operator: Nullsafe operator ``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless NullSafe Operator
	:twitter:description: Useless NullSafe Operator: Nullsafe operator ``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless NullSafe Operator
	:og:type: article
	:og:description: Nullsafe operator ``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Useless NullSafe Operator.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UselessNullSafeOperator.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UselessNullSafeOperator.html","name":"Useless NullSafe Operator","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Nullsafe operator ``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Useless NullSafe Operator.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Nullsafe operator ``?->`` has no object when the types are never null, or when coalesce is active.

The nullsafe operator protects the execution from accessing a method or a property on a null value. If the object part of the syntax cannot be null, then the nullsafe operator ``?->`` will not protect it. 

The nullsafe operator is filling the same duty as ``??`` operator, although with a more granular precision. 


.. code-block:: php
   
   <?php
   
   function foo() : A {
   	return new A(); // or other code
   }
   
   // foo() always returns A, so it is always valid
   foo()?->methodOnA();
   
   // goo() may return NULL: ?-> and ?? are filling the same duty
   goo()?->methodOnA ?? C;
   
   function goo() : ?A {}
   
   ?>
Connex PHP features
-------------------

  + `nullsafe-operator <https://php-dictionary.readthedocs.io/en/latest/dictionary/nullsafe-operator.ini.html>`_


Suggestions
___________

* Replace the null safe operator with the normal one.
* Add the type null to the type declaration.
* Check for null-coalesce operator ?? and choose the most appropriate.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UselessNullSafeOperator                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.5                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


