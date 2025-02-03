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
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Variable Variables.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/VariableVariables.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/VariableVariables.html","name":"Variable Variables","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"A variable variable takes the value of a variable and treats that as the name of a variable","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Variable Variables.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

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


