.. _variables-variablevariables:

.. _variable-variables:

Variable Variables
++++++++++++++++++

.. meta::
	:description:
		Variable Variables: A variable variable takes the value of a variable and treats that as the name of a variable.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Variable Variables
	:twitter:description: Variable Variables: A variable variable takes the value of a variable and treats that as the name of a variable
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Variable Variables
	:og:type: article
	:og:description: A variable variable takes the value of a variable and treats that as the name of a variable
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Variables/VariableVariables.html
	:og:locale: en
A variable variable takes the value of a variable and treats that as the name of a variable.

PHP has the ability to dynamically use a variable. 

They are also called 'dynamic variable'.

.. code-block:: php
   
   <?php
   
   // Normal variable
   $a = 'b';
   $b = 'c';
   
   // Variable variable
   $d = $$b;
   
   // Variable variable in string
   $d = "$\{$b\}";
   
   ?>

See also `Variable variables <https://www.php.net/manual/en/language.variables.variable.php>`_.

Connex PHP features
-------------------

  + `variable-variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable-variable.ini.html>`_
  + `variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/VariableVariables                                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
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


