.. _classes-couldbereadonlyproperty:

.. _could-be-readonly-property:

Could Be Readonly Property
++++++++++++++++++++++++++

.. meta::
	:description:
		Could Be Readonly Property: This property could be made readonly.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be Readonly Property
	:twitter:description: Could Be Readonly Property: This property could be made readonly
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be Readonly Property
	:og:type: article
	:og:description: This property could be made readonly
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Be Readonly Property.html
	:og:locale: en
This property could be made readonly. For that, the property is set in the constructor, and optionally in the ``__clone`` magic method, and never modified otherwise.

.. code-block:: php
   
   <?php
   
   class x {
   	private int $ok, $ok2;
   
   	function __construct() {
   		$this->ok = 1;
   		$this->ok2 = 1;
   	}
   	
   	function getOk2() {
   		return $this->ko;
   	}
   
   	function __clone() {
   		$this->ok2 = 1;
   	}
   }
   ?>

Suggestions
___________

* Add the readonly option to the property definition




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBeReadonlyProperty                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+


