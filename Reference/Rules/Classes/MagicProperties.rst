.. _classes-magicproperties:

.. _magic-properties:

Magic Properties
++++++++++++++++

  List of magic properties used in the code. A magic property is a property called on a object, whose class doesn't define that properties, and define the related magic properties ``__get`` and ``__set``. `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ properties cannot be magic.

Some classes define the magic methods for magic property, but do not use them. 


.. code-block:: php
   
   <?php
   
   class x {
   	public $normal = 1;
   	
   	// Two classic magic properties
   	function __get($name) {}
   
   	function __set($name, $value) {}
   }
   
   $x = new X;
   
   // Magic propery, so __set is called;
   $x->magic = 1;
   
   // Not a magic property.
   $x->normal = 2;
   
   ?>
Connex PHP features
-------------------

  + `magic-property <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-property.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MagicProperties                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Inventory <ruleset-Inventory>`                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.5                                                                                                                   |
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


