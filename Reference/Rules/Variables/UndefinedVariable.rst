.. _variables-undefinedvariable:


.. _undefined-variable:

Undefined Variable
++++++++++++++++++

.. meta::
	:description:
		Undefined Variable: Variable that is used before any initialisation.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Undefined Variable
	:twitter:description: Undefined Variable: Variable that is used before any initialisation
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Undefined Variable
	:og:type: article
	:og:description: Variable that is used before any initialisation
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Undefined Variable.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/UndefinedVariable.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/UndefinedVariable.html","name":"Undefined Variable","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 14 Jan 2025 12:52:58 +0000","dateModified":"Tue, 14 Jan 2025 12:52:58 +0000","description":"Variable that is used before any initialisation","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Undefined Variable.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Variable that is used before any initialisation. 

It is recommended to use a default value for every variable used. When not specified, the default value is set to ``NULL`` by PHP.

Variable may be created in various ways : assignation, arguments, foreach blind variables, `static <https://www.php.net/manual/en/language.oop5.static.php>`_ and global variables.

This analysis doesn't handle dynamic variables, such as ``$$x``. It also doesn't handle variables outside a method or function.

.. code-block:: php
   
   <?php
   
   // Adapted from the PHP manual
   $var = 'Bob';
   $Var = 'Joe';
   // The following line may emit a warning : Undefined variable: $undefined
   echo "$var, $Var, $undefined";      // outputs "Bob, Joe, " 
   
   ?>

See also `Variable basics <https://www.php.net/manual/en/language.variables.basics.php>`_.

Related PHP errors 
-------------------

  + `Undefined variable:  <https://php-errors.readthedocs.io/en/latest/messages/undefined-variable.html>`_



Connex PHP features
-------------------

  + `variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_


Suggestions
___________

* Remove the expression that is using the undefined variable
* Fix the variable name
* Define the variable by assigning a value to it, before using it




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/UndefinedVariable                                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.2                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


