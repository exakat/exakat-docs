.. _interfaces-usedinterfaces:

.. _used-interfaces:

Used Interfaces
+++++++++++++++

.. meta::
	:description:
		Used Interfaces: This rule lists all the interfaces used in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Used Interfaces
	:twitter:description: Used Interfaces: This rule lists all the interfaces used in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Used Interfaces
	:og:type: article
	:og:description: This rule lists all the interfaces used in the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Used Interfaces.html
	:og:locale: en
This rule lists all the interfaces used in the code. They are used with the ``implements`` keyword, the ``instanceof`` operator, and as types with parameters, class constants, properties and methods.

.. code-block:: php
   
   <?php
   
   interface used {}
   
   // Used by implementation
   class c implements used {}
   
   // Used by extension
   interface j implements used {}
   
   $x = new c;
   
   // Used in a instanceof
   var_dump($x instanceof used); 
   
   // Used in a typehint
   function foo(Used $x) {}
   
   ?>
Connex PHP features
-------------------

  + `interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/interface.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/UsedInterfaces                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


