.. _classes-nopssoutsideclass:


.. _self,-parent,-static-outside-class:

self, parent, static Outside Class
++++++++++++++++++++++++++++++++++


.. meta::

	:description:

		self, parent, static Outside Class: self, parent and static should be called inside a class or trait.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: self, parent, static Outside Class

	:twitter:description: self, parent, static Outside Class: self, parent and static should be called inside a class or trait

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: self, parent, static Outside Class

	:og:type: article

	:og:description: self, parent and static should be called inside a class or trait

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/self, parent, static Outside Class.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/NoPSSOutsideClass.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/NoPSSOutsideClass.html","name":"self, parent, static Outside Class","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 21 Jan 2025 08:40:17 +0000","dateModified":"Tue, 21 Jan 2025 08:40:17 +0000","description":"self, parent and static should be called inside a class or trait","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/self, parent, static Outside Class.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_, `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ and `static <https://www.php.net/manual/en/language.oop5.static.php>`_ should be called inside a class or trait. PHP lint won't report those situations. 

`self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_, `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ and `static <https://www.php.net/manual/en/language.oop5.static.php>`_ may be used in a trait : their actual value will be only known at execution time, when the trait is used.



Such syntax problem is only revealed at execution time : PHP raises a Fatal `error <https://www.php.net/error>`_. 

The origin of the problem is usually a method that was moved outside a class, at least temporarily. 

Closures and arrow functions are reported here, though they might be rebound with a valid context before execution.

.. code-block:: php
   
   <?php
   // In the examples, self, parent and static may be used interchangeably
   
   // This raises a Fatal error
   //Fatal error: Uncaught Error: Cannot access static:: when no class scope is active
   new static();
   
   // static calls
   echo self::CONSTANTE;
   echo self::$property;
   echo self::method();
   
   // as a type hint
   function foo(static $x) {
       doSomething();
   }
   
   // as a instanceof
   if ($x instanceof static) {
       doSomething();
   }
   
   ?>

See also `Scope Resolution Operator (::) <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_.

Related PHP errors 
-------------------

  + `Cannot access static:: when no class scope is active <https://php-errors.readthedocs.io/en/latest/messages/cannot-access-static%3A%3A-when-no-class-scope-is-active.html>`_



Connex PHP features
-------------------

  + `self <https://php-dictionary.readthedocs.io/en/latest/dictionary/self.ini.html>`_
  + `parent <https://php-dictionary.readthedocs.io/en/latest/dictionary/parent.ini.html>`_
  + `static <https://php-dictionary.readthedocs.io/en/latest/dictionary/static.ini.html>`_


Suggestions
___________

* Remove the call to static, parent or self
* Make sure the closure is correctly binded before usage




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/NoPSSOutsideClass                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.3                                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+


