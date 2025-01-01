.. _classes-incompatibleconstructor:

.. _different-constructors:

Different Constructors
++++++++++++++++++++++

.. meta::
	:description:
		Different Constructors: PHP allows different signatures for constructors.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Different Constructors
	:twitter:description: Different Constructors: PHP allows different signatures for constructors
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Different Constructors
	:og:type: article
	:og:description: PHP allows different signatures for constructors
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/IncompatibleConstructor.html
	:og:locale: en
PHP allows different signatures for constructors. This is a legacy feature. 

Only constructors are allowed to have different signatures : all other methods must be compatible with the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ methods.

.. code-block:: php
   
   <?php
   
   class x {
   	function __construct($a) {
   	}
   }
   
   class y extends x {
   	function __construct($a, $b) {
   		$this->b = $a;
   		parent::__construct($a);
   	}
   }
   
   ?>

Suggestions
___________

* Synchronize the methods signatures
* Make use of named constructors to have different signatures when building objects




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/IncompatibleConstructor                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


