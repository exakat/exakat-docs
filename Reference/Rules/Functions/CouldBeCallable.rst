.. _functions-couldbecallable:

.. _could-be-typed-callable:

Could Be Typed Callable
+++++++++++++++++++++++

.. meta::
	:description:
		Could Be Typed Callable: Those arguments may use the callable type.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be Typed Callable
	:twitter:description: Could Be Typed Callable: Those arguments may use the callable type
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be Typed Callable
	:og:type: article
	:og:description: Those arguments may use the callable type
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Be Typed Callable.html
	:og:locale: en
Those arguments may use the callable type. 

'callable' is a PHP keyword that represents callback functions. Those may be used in dynamic function call, like $function(); or as callback functions, like with `array_map() <https://www.php.net/array_map>`_;

callable may be a string representing a function name or a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ call (including \:\:), an array with two elements, (a class or object, and a method), or a `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_.

When arguments are used to call a function, but are not marked with 'callable', they are reported by this analysis.

.. code-block:: php
   
   <?php
   
   function foo(callable $callable) {
       // very simple callback
       return $callable();
   }
   
   function foo2($array, $callable) {
       // very simple callback
       return array_map($array, $callable);
   }
   
   ?>

See also `Callback / callable <https://www.php.net/manual/en/language.types.callable.php>`_.

Connex PHP features
-------------------

  + `callable <https://php-dictionary.readthedocs.io/en/latest/dictionary/callable.ini.html>`_


Suggestions
___________

* Add the type callable
* Use the function is_callable() inside the method if 'callable' is too strong.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/CouldBeCallable                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.5                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-magento-functions-couldbecallable`, :ref:`case-prestashop-functions-couldbecallable`                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


