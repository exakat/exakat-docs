.. _classes-staticcannotcallnonstatic:

.. _static-methods-cannot-call-non-static-methods:

Static Methods Cannot Call Non-Static Methods
+++++++++++++++++++++++++++++++++++++++++++++

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
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


