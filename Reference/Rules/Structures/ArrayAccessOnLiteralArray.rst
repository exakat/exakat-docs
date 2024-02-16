.. _structures-arrayaccessonliteralarray:

.. _array-access-on-literal-array:

Array Access On Literal Array
+++++++++++++++++++++++++++++

  Accessing an element on a literal array makes that array non-reusable. 

It is recommended to make this array a constant or a property, for easier reusage. It also make that content more visiblem in the class definitions.

.. code-block:: php
   
   <?php
   
   class Suit {
   	const NAMES = ['Club' => 1, 'Spade' => 2, 'Heart' => 3, 'Diamond' => 4];
   
   	function __construct($name) {
   		if (!isset(self::NAMES[$name]) {
   			throw new Exception('Not a suit color');
   		}
   	}
   }
   
   class HiddenSuitList {
   	function __construct($name) {
   		if (!isset(['Club' => 1, 'Spade' => 2, 'Heart' => 3, 'Diamond' => 4][$name]) {
   			throw new Exception('Not a suit color');
   		}
   	}
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ArrayAccessOnLiteralArray                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Semantics <ruleset-Semantics>`                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


