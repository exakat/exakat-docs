.. _classes-staticcannotcallnonstatic:

.. _static-methods-cannot-call-non-static-methods:

Static Methods Cannot Call Non-Static Methods
+++++++++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Static Methods Cannot Call Non-Static Methods: A static method cannot call a non-static method.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Static Methods Cannot Call Non-Static Methods
	:twitter:description: Static Methods Cannot Call Non-Static Methods: A static method cannot call a non-static method
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Static Methods Cannot Call Non-Static Methods
	:og:type: article
	:og:description: A static method cannot call a non-static method
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Static Methods Cannot Call Non-Static Methods.html
	:og:locale: en
A `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method cannot call a non-`static <https://www.php.net/manual/en/language.oop5.static.php>`_ method. The object context would be missing. 

On the other hand, a method may call a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method, as the context is lost, but not useful. 

Magic methods cannot be `static <https://www.php.net/manual/en/language.oop5.static.php>`_, so they are out of this rule. This applies to the constructor, when called with ``parent\:\:`__construct() <https://www.php.net/manual/en/language.oop5.decon.php>`_``.


.. code-block:: php
   
   <?php
   
   class x {
   	function foo() {}
   
   	static function ioo() {
   		// This syntax is valid within a class
   		// yet, the call is not possible
   		self::foo();
   	}
   
   }
   ?>
Related PHP errors 
-------------------

  + `Non-static method %s::%s() cannot be called statically <https://php-errors.readthedocs.io/en/latest/messages/non-static-method-%25s%5C%3A%5C%3A%25s%5C%28%5C%29-cannot-be-called-statically.html>`_




Suggestions
___________

* Make the calling method non static too
* Remove the call to the non-static method
* Make the target method static




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/StaticCannotCallNonStatic                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


