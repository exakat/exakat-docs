.. _complete-variabletypehint:

.. _variable-anf-property-typehint:

Variable Anf Property Typehint
++++++++++++++++++++++++++++++

.. meta::
	:description:
		Variable Anf Property Typehint: Adds typehints to (local) variables and properties, by inference from the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Variable Anf Property Typehint
	:twitter:description: Variable Anf Property Typehint: Adds typehints to (local) variables and properties, by inference from the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Variable Anf Property Typehint
	:og:type: article
	:og:description: Adds typehints to (local) variables and properties, by inference from the code
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Complete/VariableTypehint.html
	:og:locale: en
Adds typehints to (local) variables and properties, by inference from the code. 

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
  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_


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


