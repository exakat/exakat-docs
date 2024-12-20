.. _classes-untypednodefaultproperties:

.. _untyped-no-default-properties:

Untyped No Default Properties
+++++++++++++++++++++++++++++

  This rule reports untyped properties without default value, that are not assigned at constructor time. 

This means that these properties will be assigned later, and are now running the risk to be accessed before being written. This yields a warning, and, when the property get typed, event with ``mixed``, a fatal `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
   
   class x {
   	public $noTypeNoDefaultNoConstructor;
   	public $noTypeNoDefaultButConstructor;
   	
   	function __construct() {
   		// property is defined in the constructor, so always defined
   		$this->noTypeNoDefaultButConstructor = 1;
   	}
   	
   	function foo()  {
   		// possible error here
   		return $this->noTypeNoDefaultNoConstructor;
   	}
   }
   ?>
Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Typed+property+x%3A%3A%24p2+must+not+be+accessed+before+initialization.html>`_



Connex PHP features
-------------------

  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UntypedNoDefaultProperties                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Class Review <ruleset-Class-Review>`                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.2                                                                                                                   |
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


