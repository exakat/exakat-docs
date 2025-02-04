.. _classes-checkafternullsafeoperator:


.. _check-after-null-safe-operator:

Check After Null Safe Operator
++++++++++++++++++++++++++++++

.. meta::
	:description:
		Check After Null Safe Operator: Null-safe operator is ``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Check After Null Safe Operator
	:twitter:description: Check After Null Safe Operator: Null-safe operator is ``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Check After Null Safe Operator
	:og:type: article
	:og:description: Null-safe operator is ``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Check After Null Safe Operator.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CheckAfterNullSafeOperator.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CheckAfterNullSafeOperator.html","name":"Check After Null Safe Operator","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Null-safe operator is ``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Check After Null Safe Operator.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`Null <https://www.php.net/`null <https://www.php.net/null>`_>`_-safe operator is ``?->``, which prevents fatal errors in case the object of the call is `NULL <https://www.php.net/manual/en/language.types.`null <https://www.php.net/null>`_.php>`_. The execution continues, though the `result <https://www.php.net/result>`_ of the expression is now `NULL <https://www.php.net/manual/en/language.types.`null <https://www.php.net/null>`_.php>`_ too. 

While it saves some checks in certain cases, the `null <https://www.php.net/`null <https://www.php.net/null>`_>`_-safe operator should be followed by a check on the returned value to process any misfire of the method. 

This analysis checks that the `result <https://www.php.net/result>`_ of the expression is collected, and compared to `null <https://www.php.net/`null <https://www.php.net/null>`_>`_.

.. code-block:: php
   
   <?php
   
   $result = $object?->foo(); 
   
   if ($result === null) {
   	throw new ObjectException(The object could not call $foo\n);
   }
   
   ?>
Connex PHP features
-------------------

  + `Null Safe Object Operator <https://php-dictionary.readthedocs.io/en/latest/dictionary/nullsafe-object-operator.ini.html>`_


Suggestions
___________

* Collect and check the result of the expression to null
* Remove the null-safe operator and check before calling the object's method or property




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CheckAfterNullSafeOperator                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                                                             |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+


