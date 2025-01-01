.. _structures-catchshadowsvariable:

.. _catch-overwrite-variable:

Catch Overwrite Variable
++++++++++++++++++++++++

.. meta::
	:description:
		Catch Overwrite Variable: The try/catch structure uses some variables that are also in use in this scope.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Catch Overwrite Variable
	:twitter:description: Catch Overwrite Variable: The try/catch structure uses some variables that are also in use in this scope
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Catch Overwrite Variable
	:og:type: article
	:og:description: The try/catch structure uses some variables that are also in use in this scope
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/CatchShadowsVariable.html
	:og:locale: en
The try/catch structure uses some variables that are also in use in this scope. In case of a caught `exception <https://www.php.net/exception>`_, the `exception <https://www.php.net/exception>`_ will be put in the catch variable, and overwrite the current value, loosing some data.
It is recommended to use another name for these catch variables.

.. code-block:: php
   
   <?php
   
   // variables and caught exceptions are distinct
   $argument = 1;
   try {
       methodThatMayRaiseException($argument);
   } (Exception $e) {
       // here, $e has been changed to an exception.
   }
   
   // variables and caught exceptions are overlapping
   $e = 1;
   try {
       methodThatMayRaiseException();
   } (Exception $e) {
       // here, $e has been changed to an exception.
   }
   
   ?>
Connex PHP features
-------------------

  + `try-catch <https://php-dictionary.readthedocs.io/en/latest/dictionary/try-catch.ini.html>`_


Suggestions
___________

* Use a standard : only use $e (or else) to catch exceptions. Avoid using them for anything else, parameter, property or local variable.
* Change the variable, and keep the caught exception




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CatchShadowsVariable                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-catch-overwrite <https://github.com/dseguy/clearPHP/tree/master/rules/no-catch-overwrite.md>`__                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phpipam-structures-catchshadowsvariable`, :ref:`case-suitecrm-structures-catchshadowsvariable`               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


