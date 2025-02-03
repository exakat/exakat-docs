.. _functions-cannotusestaticforclosure:


.. _cannot-use-static-for-closure:

Cannot Use Static For Closure
+++++++++++++++++++++++++++++


.. meta::

	:description:

		Cannot Use Static For Closure: The reported closures and arrow functions cannot use the static keyword.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Cannot Use Static For Closure

	:twitter:description: Cannot Use Static For Closure: The reported closures and arrow functions cannot use the static keyword

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Cannot Use Static For Closure

	:og:type: article

	:og:description: The reported closures and arrow functions cannot use the static keyword

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Cannot Use Static For Closure.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/CannotUseStaticForClosure.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/CannotUseStaticForClosure.html","name":"Cannot Use Static For Closure","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"The reported closures and arrow functions cannot use the static keyword","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Cannot Use Static For Closure.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The reported closures and arrow functions cannot use the `static <https://www.php.net/manual/en/language.oop5.static.php>`_ keyword. 

Closures that makes use of the `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ pseudo-variable cannot use the `static <https://www.php.net/manual/en/language.oop5.static.php>`_ keyword, at it prevents the import of the `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ context in the `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_. It will fail at execution.

Closures that makes use of the bindTo() method, to change the context of execution, also cannot use the `static <https://www.php.net/manual/en/language.oop5.static.php>`_ keyword. Even if `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ is not used in the `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_, the `static <https://www.php.net/manual/en/language.oop5.static.php>`_ keyword prevents the call to bindTo().

.. code-block:: php
   
   <?php
   
   class x {
       function foo() {
           // Not possible, $this is now undefined in the body of the closure
           static function () { return $this->a;};
       }
   
       function foo2() {
           // Not possible, $this is now undefined in the body of the arrow function
           static fn () => $this->a;
       }
       
       function foo3() {
           // Not possible, the closure gets a new context before being called.
           $a = static fn () => $ba;
           $this->foo4($a);
       }
       
       function foo4($c) {
           $c->bindTo($this);
           $c();
       }
       
   }
   ?>

See also `Static anonymous functions <https://www.php.net/manual/en/functions.anonymous.php#functions.anonymous-functions.static>`_.

Related PHP errors 
-------------------

  + `Cannot bind an instance to a static closure <https://php-errors.readthedocs.io/en/latest/messages/cannot-bind-an-instance-to-a-static-closure.html>`_



Connex PHP features
-------------------

  + `closure <https://php-dictionary.readthedocs.io/en/latest/dictionary/closure.ini.html>`_
  + `static <https://php-dictionary.readthedocs.io/en/latest/dictionary/static.ini.html>`_


Suggestions
___________

* Remove the static keyword
* Remove the call to bindTo() method
* Remove the usage of the $this variable




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/CannotUseStaticForClosure                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


