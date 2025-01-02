.. _extensions-extuopz:

.. _ext-uopz:

ext/uopz
++++++++

.. meta::
	:description:
		ext/uopz: Extension UOPZ : User Operations for Zend.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/uopz
	:twitter:description: ext/uopz: Extension UOPZ : User Operations for Zend
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/uopz
	:og:type: article
	:og:description: Extension UOPZ : User Operations for Zend
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/uopz.html
	:og:locale: en
Extension UOPZ : User Operations for Zend.

The uopz extension is focused on providing utilities to aid with unit testing PHP code.

It supports the following activities: Intercepting function execution, Intercepting object creation, Hooking into function execution, Manipulation of function statics, Manipulation of function flags, Redefinition of constants, Deletion of constants, Runtime creation of functions and methods,

.. code-block:: php
   
   <?php
   // The example is extracted from the UOPZ extension test suite : tests/001.phpt
   class Foo {
   	public function bar(int $arg) : int {
   		return $arg;
   	}
   }
   var_dump(uopz_set_return(Foo::class, 'bar', true));
   $foo = new Foo();
   var_dump($foo->bar(1));
   uopz_set_return(Foo::class, 'bar', function(int $arg) : int {
   	return $arg * 2;
   }, true);
   var_dump($foo->bar(2));
   try {
   	uopz_set_return(Foo::class, 'nope', 1);
   } catch(Throwable $t) {
   	var_dump($t->getMessage());
   }
   class Bar extends Foo {}
   try {
   	uopz_set_return(Bar::class, 'bar', null);
   } catch (Throwable $t) {
   	var_dump($t->getMessage());
   }
   
   	uopz_set_something(Bar::class, 'bar', null);
   
   ?>

See also `ext/uopz <https://pecl.php.net/package/uopz>`_ and `User Operations for Zend <https://github.com/krakjoe/uopz>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extuopz                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.7                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


