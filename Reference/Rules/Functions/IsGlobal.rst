.. _functions-isglobal:

.. _functioncall-is-global:

Functioncall Is Global
++++++++++++++++++++++

.. meta::
	:description:
		Functioncall Is Global: Marks a functioncall when it is from the global scope.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Functioncall Is Global
	:twitter:description: Functioncall Is Global: Marks a functioncall when it is from the global scope
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Functioncall Is Global
	:og:type: article
	:og:description: Marks a functioncall when it is from the global scope
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Functioncall Is Global.html
	:og:locale: en
Marks a functioncall when it is from the global scope. It is not located in another function, class or trait.

.. code-block:: php
   
   <?php
   
   function foo() {
   	// This is not a global functioncall
   	goo();
   }
   
   // This is a global functioncall
   foo();
   
   ?>

See also `class <https://www.php.net/manual/en/language.oop5.basic.php#language.oop5.basic.class>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/IsGlobal                                                                                                      |
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


