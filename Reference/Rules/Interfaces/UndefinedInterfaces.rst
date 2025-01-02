.. _interfaces-undefinedinterfaces:

.. _undefined-interfaces:

Undefined Interfaces
++++++++++++++++++++

.. meta::
	:description:
		Undefined Interfaces: Some types or ``instanceof`` that are relying on undefined interfaces or classes: the validation of the type will always fail and return false.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Undefined Interfaces
	:twitter:description: Undefined Interfaces: Some types or ``instanceof`` that are relying on undefined interfaces or classes: the validation of the type will always fail and return false
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Undefined Interfaces
	:og:type: article
	:og:description: Some types or ``instanceof`` that are relying on undefined interfaces or classes: the validation of the type will always fail and return false
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Undefined Interfaces.html
	:og:locale: en
Some types or ``instanceof`` that are relying on undefined interfaces or classes: the validation of the type will always fail and return false. Any condition based upon them are dead code.

.. code-block:: php
   
   <?php
   
   class var implements undefinedInterface {
       // If undefinedInterface is undefined, this code lints but doesn't run
   }
   
   if ($o instanceof undefinedInterface) {
       // This is silent dead code
   }
   
   function foo(undefinedInterface $a) {
       // This is dead code
       // it will probably be discovered at execution
   }
   
   ?>

See also `Object interfaces <https://www.php.net/manual/en/language.oop5.interfaces.php>`_, `Type declarations <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration>`_ and `Instanceof <https://www.php.net/manual/en/language.operators.type.php>`_.

Related PHP errors 
-------------------

  + `Argument #1 ($a) must be of type T <https://php-errors.readthedocs.io/en/latest/messages/argument-%23%25d-%5C%28%24%25s%5C%29-must-be-of-type-%25s%5C%2C-%25s-given.html>`_



Connex PHP features
-------------------

  + `interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/interface.ini.html>`_


Suggestions
___________

* Implement the missing interfaces
* Remove the code governed by the missing interface : the whole method if it is an typehint, the whole if/then if it is a condition.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/UndefinedInterfaces                                                                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-xataface-interfaces-undefinedinterfaces`                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


