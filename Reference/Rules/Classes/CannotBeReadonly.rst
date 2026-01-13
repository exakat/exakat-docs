.. _classes-cannotbereadonly:

.. _property-cannot-be-readonly:

Property Cannot Be Readonly
+++++++++++++++++++++++++++

  This analysis reports different situations where a property is readonly, and has some impossible code. 

Two cases are reported : 
+ a `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_-updated property, where it is updated with a value that is created from itself. The most obvious is ``$this->a = `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_->a;`` (which is reported as an `error <https://www.php.net/error>`_ by PHP), and ``$this->a = foo(`$this <https://www.php.net/manual/en/language.oop5.basic.php>`_->a);`` is the most common.
+ a property which is set in the constructor, yet has a distinct method where it is updated too. 

Most of thoses cases are dead code.

.. code-block:: php
   
   <?php
   
   class x {
   	private readonly $p;
   	private readonly $q;
   	
   	function __construct($p) {
   		$this->p = $p; // normal assignation
   	}
   	
   	function foo() {
   		$this->q = bar($this->q); // this is not possible with readonly
   		$this->q++; // this is not possible with readonly
   		$this->q[] = 2; // this is not possible with readonly
   	}
   }
   
   ?>
Connex PHP features
-------------------

  + `readonly <https://php-dictionary.readthedocs.io/en/latest/dictionary/readonly.ini.html>`_
  + `dead-code <https://php-dictionary.readthedocs.io/en/latest/dictionary/dead-code.ini.html>`_


Suggestions
___________

* Remove the impossible code




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CannotBeReadonly                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.1                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


