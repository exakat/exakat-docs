.. _functions-typehintmustbereturned:


.. _type-must-be-returned:

Type Must Be Returned
+++++++++++++++++++++

.. meta::
	:description:
		Type Must Be Returned: When using a type for a method, it is compulsory to use a at least one return in the method's body.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Type Must Be Returned
	:twitter:description: Type Must Be Returned: When using a type for a method, it is compulsory to use a at least one return in the method's body
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Type Must Be Returned
	:og:type: article
	:og:description: When using a type for a method, it is compulsory to use a at least one return in the method's body
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Type Must Be Returned.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/TypehintMustBeReturned.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/TypehintMustBeReturned.html","name":"Type Must Be Returned","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"When using a type for a method, it is compulsory to use a at least one return in the method's body","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Type Must Be Returned.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When using a type for a method, it is compulsory to use a at least one return in the method's body. This is true for nullable type too : ``return`` alone won't be sufficient.

When the method contains a return expression, PHP doesn't lint unless the return expression has a value. Any value will do, and it will actually checked at execution time.

When the method contains no return expression, PHP only checks it at execution time. 

There is no need for a return expression when the method throws an expression, yield values, triggers an `error <https://www.php.net/error>`_ or triggers an assertion. Even in case of inheritance or implementation, the return type may be replaced by ``never``.

.. code-block:: php
   
   <?php
   
   // The function returns a value (here, correct object)
   function foo() : Bar { return new Bar(); }
   
   // The function should at least, return a value
   function foo() : Bar { }
   
   // The function should at least, return a value : Null or an object. Void, here, is not acceptable.
   function foo() : ?Bar { return; }
   
   ?>

See also `Return Type Declaration <https://www.php.net/manual/en/functions.returning-values.php#functions.returning-values.type-declaration>`_ and `Type hint in PHP function parameters and return values <https://mlocati.github.io/articles/php-type-hinting.html>`_.

Related PHP errors 
-------------------

  + `A function with return type must return a value <https://php-errors.readthedocs.io/en/latest/messages/a-function-with-return-type-must-return-a-value.html>`_
  + `A never-returning function must not return <https://php-errors.readthedocs.io/en/latest/messages/a-never-returning-%25s-must-not-return.html>`_



Connex PHP features
-------------------

  + `return-type <https://php-dictionary.readthedocs.io/en/latest/dictionary/return-type.ini.html>`_
  + `never-type <https://php-dictionary.readthedocs.io/en/latest/dictionary/never-type.ini.html>`_


Suggestions
___________

* Add a return with a valid value
* Add a throw expression
* Add a trigger_error() call
* Add a assert(false, ...) expression
* If the method doesn't return, change the returntype to `never`




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/TypehintMustBeReturned                                                                                                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.9                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


