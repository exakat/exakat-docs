.. _structures-globalinglobal:

.. _global-in-global:

Global In Global
++++++++++++++++

.. meta::
	:description:
		Global In Global: List of global variables.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Global In Global
	:twitter:description: Global In Global: List of global variables
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Global In Global
	:og:type: article
	:og:description: List of global variables
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Global In Global.html
	:og:locale: en
List of global variables. There are the global variables, defined with the global keyword, and the implicit global variables, defined in the global scope.

.. code-block:: php
   
   <?php
       global $explicitGlobal; // in global namespace
       
       $implicitGlobal = 1; // in global namespace, variables are automatically global
       
       function foo() {
           global $explicitGlobalInFoo; // in functions, globals must be declared with global
       }
   ?>

See also `Variable Scope <https://www.php.net/manual/en/language.variables.scope.php>`_.

Connex PHP features
-------------------

  + `global <https://php-dictionary.readthedocs.io/en/latest/dictionary/global.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/GlobalInGlobal                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


