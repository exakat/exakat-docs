.. _complete-variabletypehint:

.. _variable-and-property-type:

Variable And Property Type
++++++++++++++++++++++++++

.. meta::
	:description:
		Variable And Property Type: Adds types to (local) variables and properties, by inference from the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Variable And Property Type
	:twitter:description: Variable And Property Type: Adds types to (local) variables and properties, by inference from the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Variable And Property Type
	:og:type: article
	:og:description: Adds types to (local) variables and properties, by inference from the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Variable And Property Type.html
	:og:locale: en
Adds types to (local) variables and properties, by inference from the code. 

Currently, the variable must be assigned only one type within its context to be typed. Non-typed variables limit the scope of other rules.

This is an internal tool, to help find definitions of classes. The same strategies may happen to arguments, though there is no syntax relay for variables.

.. code-block:: php
   
   <?php
   
   function foo() {
       $a = 1;
       
       return $a;
   }
   
   ?>
Connex PHP features
-------------------

  + `variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_
  + `type <https://php-dictionary.readthedocs.io/en/latest/dictionary/type.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/VariableTypehint                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`First <ruleset-First>`, :ref:`NoDoc <ruleset-NoDoc>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.2                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+


