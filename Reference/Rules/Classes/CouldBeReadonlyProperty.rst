.. _classes-couldbereadonlyproperty:

.. _could-be-readonly-property:

Could Be Readonly Property
++++++++++++++++++++++++++

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

+--------------+----------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBeReadonlyProperty                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+----------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                           |
+--------------+----------------------------------------------------------------------------------------------------------------+
| Available in |                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------+


