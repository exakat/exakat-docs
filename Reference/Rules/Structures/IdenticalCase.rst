.. _structures-identicalcase:

.. _identical-case-in-switch:

Identical Case In Switch
++++++++++++++++++++++++

  In a `switch() <https://www.php.net/manual/en/control-structures.switch.php>`_ or `match() <https://www.php.net/manual/en/control-structures.match.php>`_ statement, when there are identical cases, it means that multiple case labels that have the same code block. 

This can happen by mistake or design. They may be merged together.

.. code-block:: php
   
   <?php
   
   switch($a) {
   	case 1: 
   		$b = 2;
   		break;
   
   	case 2: 
   		$b = 12;
   		break;
   
   	// Identical to case 1
   	case 3: 
   		$b = 2;
   		break;
   }
   
   ?>

Suggestions
___________

* Merge the cases and reduce the size of code
* Review the cases code and make them different




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/IdenticalCase                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | dry                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


