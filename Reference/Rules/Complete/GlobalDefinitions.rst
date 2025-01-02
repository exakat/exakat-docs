.. _complete-globaldefinitions:

.. _global-definitions:

Global Definitions
++++++++++++++++++

.. meta::
	:description:
		Global Definitions: Sets the definitions of global variables across the application.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Global Definitions
	:twitter:description: Global Definitions: Sets the definitions of global variables across the application
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Global Definitions
	:og:type: article
	:og:description: Sets the definitions of global variables across the application
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Global Definitions.html
	:og:locale: en
Sets the definitions of global variables across the application.

It creates a Virtualglobal atom, which links to all definitions of that variables, using ``global $a`` or ``$GLOBALS['a']``.

It currently doesn't work with variables in the global space, as it is not known how to detect them : they might be included at some point.

.. code-block:: php
   
   <?php
   
   function foo() {
   	global $a;
   	
   	$a = 'PHP';
   }
   
   function goo() {
   	echo $GLOBALS['a'];
   }
   
   
   ?>
Connex PHP features
-------------------

  + `global <https://php-dictionary.readthedocs.io/en/latest/dictionary/global.ini.html>`_
  + `globals <https://php-dictionary.readthedocs.io/en/latest/dictionary/globals.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/GlobalDefinitions                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


