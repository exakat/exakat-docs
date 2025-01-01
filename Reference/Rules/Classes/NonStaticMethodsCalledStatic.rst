.. _classes-nonstaticmethodscalledstatic:

.. _non-static-methods-called-in-a-static:

Non Static Methods Called In A Static
+++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Non Static Methods Called In A Static: Static methods have to be declared as such (using the static keyword).
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Non Static Methods Called In A Static
	:twitter:description: Non Static Methods Called In A Static: Static methods have to be declared as such (using the static keyword)
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Non Static Methods Called In A Static
	:og:type: article
	:og:description: Static methods have to be declared as such (using the static keyword)
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/NonStaticMethodsCalledStatic.html
	:og:locale: en
`Static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods have to be declared as such (using the `static <https://www.php.net/manual/en/language.oop5.static.php>`_ keyword). Then, one may call them without instantiating the object.

PHP 7.0, and more recent versions, yield a deprecated `error <https://www.php.net/error>`_ : ``Non-`static <https://www.php.net/manual/en/language.oop5.static.php>`_ method A\:\:B() should not be called statically``.

PHP 5 and older doesn't check that a method is `static <https://www.php.net/manual/en/language.oop5.static.php>`_ or not : at any point, the code may call one method statically.
It is a bad idea to call non-`static <https://www.php.net/manual/en/language.oop5.static.php>`_ method statically. Such method may make use of special
variable `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_, which will be undefined. PHP will not check those calls at compile time,
nor at running time. 

It is recommended to update this situation : make the method actually `static <https://www.php.net/manual/en/language.oop5.static.php>`_, or use it only 
in object context.

Note that this analysis reports all `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method call made on a non-`static <https://www.php.net/manual/en/language.oop5.static.php>`_ method,
even within the same class or class hierarchy. PHP silently accepts `static <https://www.php.net/manual/en/language.oop5.static.php>`_ call to any
in-family method.

.. code-block:: php
   
   <?php
       class x {
           static public function sm( ) { echo __METHOD__.\n; }
           public public sm( ) { echo __METHOD__.\n; }
       } 
       
       x::sm( ); // echo x::sm 
       
       // Dynamic call
       ['x', 'sm']();
       [\x::class, 'sm']();
   
       $s = 'x::sm';
       $s();
   
   ?>

See also `Static Keyword <https://www.php.net/manual/en/language.oop5.static.php>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Non-static+method+A%3A%3AB%28%29+should+not+be+called+statically.html>`_



Connex PHP features
-------------------

  + `static <https://php-dictionary.readthedocs.io/en/latest/dictionary/static.ini.html>`_


Suggestions
___________

* Call the method the correct way
* Define the method as static




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/NonStaticMethodsCalledStatic                                                                                                                                                                                                                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                                                                                                                                                                                                                                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolphin-classes-nonstaticmethodscalledstatic`, :ref:`case-magento-classes-nonstaticmethodscalledstatic`                                                                                                                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


