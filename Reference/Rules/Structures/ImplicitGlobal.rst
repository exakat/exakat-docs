.. _structures-implicitglobal:

.. _implicit-global:

Implicit Global
+++++++++++++++

.. meta::
	:description:
		Implicit Global: Global variables, that are used in local scope with global keyword, but are not declared as global in the global scope.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Implicit Global
	:twitter:description: Implicit Global: Global variables, that are used in local scope with global keyword, but are not declared as global in the global scope
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Implicit Global
	:og:type: article
	:og:description: Global variables, that are used in local scope with global keyword, but are not declared as global in the global scope
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Implicit Global.html
	:og:locale: en
Global variables, that are used in local scope with global keyword, but are not declared as global in the global scope. They may be mistaken with distinct values, while, in PHP, variables in the global scope are truly global.

.. code-block:: php
   
   <?php
   
   // This is implicitely global
   $implicitGlobal = 1;
   
   global $explicitGlobal;
   $explicitGlobal = 2;
   
   foo();
   echo $explicitFunctionGlobal;
   
   function foo() {
       // This global is needed, but not the one in the global space
       global $implicitGlobal, $explicitGlobal, $explicitFunctionGlobal;
       
       // This won't be a global, as it must be 'global' in a function scope
       $notImplicitGlobal = 3;
       $explicitFunctionGlobal = 3;
   }
   
   ?>
Connex PHP features
-------------------

  + `global <https://php-dictionary.readthedocs.io/en/latest/dictionary/global.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ImplicitGlobal                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
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


