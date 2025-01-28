.. _classes-untypednodefaultproperties:

.. _untyped-no-default-properties:

Untyped No Default Properties
+++++++++++++++++++++++++++++

.. meta::
	:description:
		Untyped No Default Properties: This rule reports untyped properties without default value, that are not assigned at constructor time.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Untyped No Default Properties
	:twitter:description: Untyped No Default Properties: This rule reports untyped properties without default value, that are not assigned at constructor time
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Untyped No Default Properties
	:og:type: article
	:og:description: This rule reports untyped properties without default value, that are not assigned at constructor time
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Untyped No Default Properties.html
	:og:locale: en
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

  + `Typed property %s::$%s must not be accessed before initialization <https://php-errors.readthedocs.io/en/latest/messages/typed-property-%25s%3A%3A%24%25s-must-not-be-accessed-before-initialization.html>`_



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


