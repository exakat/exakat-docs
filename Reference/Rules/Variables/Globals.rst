.. _variables-globals:

.. _globals:

Globals
+++++++

.. meta::
	:description:
		Globals: Global variables.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Globals
	:twitter:description: Globals: Global variables
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Globals
	:og:type: article
	:og:description: Global variables
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Globals.html
	:og:locale: en
Global variables.

.. code-block:: php
   
   <?php
   
   // global via global keyword
   global $a, $b;
   
   // global via $GLOBALS variable
   $GLOBALS['c'] = 1;
   
   ?>

See also `Global keyword <https://www.php.net/manual/en/language.variables.scope.php#language.variables.scope.global>`_.

Connex PHP features
-------------------

  + `global <https://php-dictionary.readthedocs.io/en/latest/dictionary/global.ini.html>`_
  + `global-variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/global-variable.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/Globals                                                                                                       |
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
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


