.. _classes-classinvasion:

.. _class-invasion:

Class Invasion
++++++++++++++

  Class invasion happens when an object access another object's private methods or properties. 

This is possible from the scope of the class itself. For example, an cloned object, or a parameter with the same type as the current class. 

Class invasion is a PHP feature. 
This applies to properties, constants and methods, `static <https://www.php.net/manual/en/language.oop5.static.php>`_ or not.

.. code-block:: php
   
   <?php
   
   class x {
   	private $p = 1;
   	
   	function foo(X $x) {
   		// This is the normal access to private properties.
   		$this->p = 3; 
   		// This is class invasion, as $x is a distinct object.
   		$x->p = 2;
   	}
   }
   
   ?>
Connex PHP features
-------------------

  + `class-invasion <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-invasion.ini.html>`_


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ClassInvasion                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.1                                                                                                                    |
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


