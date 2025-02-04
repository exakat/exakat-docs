.. _structures-couldusenullableoperator:


.. _could-use-null-safe-object-operator:

Could Use Null-Safe Object Operator
+++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Could Use Null-Safe Object Operator: When the preceding function call has the potential to return null, employing the null-safe object operator can help mitigate fatal errors.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Use Null-Safe Object Operator
	:twitter:description: Could Use Null-Safe Object Operator: When the preceding function call has the potential to return null, employing the null-safe object operator can help mitigate fatal errors
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Use Null-Safe Object Operator
	:og:type: article
	:og:description: When the preceding function call has the potential to return null, employing the null-safe object operator can help mitigate fatal errors
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Use Null-Safe Object Operator.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldUseNullableOperator.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldUseNullableOperator.html","name":"Could Use Null-Safe Object Operator","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"When the preceding function call has the potential to return null, employing the null-safe object operator can help mitigate fatal errors","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Use Null-Safe Object Operator.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When the preceding function call has the potential to return `null <https://www.php.net/`null <https://www.php.net/null>`_>`_, employing the `null <https://www.php.net/`null <https://www.php.net/null>`_>`_-safe object operator can help mitigate fatal errors.

One approach is to assess the returned value prior to utilization, ensuring it is not `null <https://www.php.net/`null <https://www.php.net/null>`_>`_, and refraining from invoking methods on a `null <https://www.php.net/`null <https://www.php.net/null>`_>`_ reference. Alternatively, the `null <https://www.php.net/`null <https://www.php.net/null>`_>`_-safe operator can be employed, allowing verification of the end `result <https://www.php.net/result>`_. If the `result <https://www.php.net/result>`_ is `null <https://www.php.net/`null <https://www.php.net/null>`_>`_, it indicates an `error <https://www.php.net/error>`_.

Another approach is to use the `null <https://www.php.net/`null <https://www.php.net/null>`_>`_-safe operator when the intermediate methods returns an object or a `null <https://www.php.net/`null <https://www.php.net/null>`_>`_. When chained, the `null <https://www.php.net/`null <https://www.php.net/null>`_>`_-safe operator will prevent Fatal `Error <https://www.php.net/error>`_. 


.. code-block:: php
   
   <?php
   
   // direct usage, with a check on the final value
   $a = foo()?->b() ?? throw new exception('something went wrong when calculating $a');
      // throw as an expression is a PHP 8.0 code
   
   // direct usage, may yield a Fatal error
   foo()->b();
   
   // indirect usage, with a check on the returned value
   $a = foo();
   $c = $a ? $a->b() : null;
   
   function foo() : ?A {
       return rand(0, 1) ? new A() : null;
   }
   
   class A {
       function b() : string { return '';}
   }
   
   ?>

See also `PHP 8.0 feature focus: nullsafe methods <https://platform.sh/blog/2020/php-80-feature-focus-type-nullsafe-methods/>`_ and `Nullsafe methods and properties <https://www.php.net/manual/en/language.oop5.basic.php#language.oop5.basic.nullsafe>`_.

Related PHP errors 
-------------------

  + `Call to a member function %s() on %s <https://php-errors.readthedocs.io/en/latest/messages/call-to-a-member-function-%25s%28%29-on-%25s.html>`_
  + `Attempt to read property "%s" on %s <https://php-errors.readthedocs.io/en/latest/messages/attempt-to-read-property-%22%25s%22-on-%25s.html>`_



Connex PHP features
-------------------

  + `Null Safe Object Operator <https://php-dictionary.readthedocs.io/en/latest/dictionary/nullsafe-object-operator.ini.html>`_
  + `Nullable <https://php-dictionary.readthedocs.io/en/latest/dictionary/nullable.ini.html>`_


Suggestions
___________

* Add a check on NULL before using the returned value
* Update the previous method to prevent it from returning null
* Use the null-safe object operator and test the result afterward




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CouldUseNullableOperator                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


