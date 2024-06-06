.. _attributes-uselessoverride:

.. _useless-override-attribute:

Useless Override Attribute
++++++++++++++++++++++++++

  The `override <https://www.php.net/override>`_ `attribute <https://www.php.net/attribute>`_ is only useful on an extended class. It allows to mark a method that must be overriding a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ method. When the class is not extending another class, there is no point in using this `attribute <https://www.php.net/attribute>`_. 

This is also valid with extended class : the top `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class has no use of the `override <https://www.php.net/override>`_. 

There is a dedicated compile-time `error <https://www.php.net/error>`_.


.. code-block:: php
   
   <?php
   
   class x {
   	// override in that trait are useless
   	use t;
   	
   	// This is useless
   	#[Override]
   	function foo() {}
   }
   
   trait t {
   	// This is useless if loaded in a root class
   	#[Override]
   	function foo() {}
   }
   
   enum e {
   	// This is useless in any case
   	#[Override]
   	function foo() {}
   }
   
   
   ?>

Specs
_____

+--------------+----------------------------------------------------------------------------------------------------+
| Short name   | Attributes/UselessOverride                                                                         |
+--------------+----------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Attributes <ruleset-Attributes>` |
+--------------+----------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.8                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                       |
+--------------+----------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                               |
+--------------+----------------------------------------------------------------------------------------------------+
| Available in |                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------+


