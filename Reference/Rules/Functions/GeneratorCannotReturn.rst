.. _functions-generatorcannotreturn:

.. _generator-cannot-return:

Generator Cannot Return
+++++++++++++++++++++++

.. meta\:\:
	:description:
		Generator Cannot Return: Generators could not use return and yield at the same time.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Generator Cannot Return
	:twitter:description: Generator Cannot Return: Generators could not use return and yield at the same time
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Generator Cannot Return
	:og:type: article
	:og:description: Generators could not use return and yield at the same time
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Functions/GeneratorCannotReturn.html
	:og:locale: en
  Generators could not use return and yield at the same time. In PHP 7.0, `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_ can now use both of them.

.. code-block:: php
   
   <?php
   
   // This is not allowed until PHP 7.0
   function foo() {
       yield 1;
       return 'b';
   }
   
   ?>
Connex PHP features
-------------------

  + `generator <https://php-dictionary.readthedocs.io/en/latest/dictionary/generator.ini.html>`_


Suggestions
___________

* Remove the return




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/GeneratorCannotReturn                                                                                                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.7                                                                                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                                                                                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


