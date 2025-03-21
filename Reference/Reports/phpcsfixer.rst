.. _report-phpcsfixer:

Phpcsfixer
++++++++++

Phpcsfixer
__________

.. meta::
	:description:
		Phpcsfixer: The Phpcsfixer report provides a configuration file for php-cs-fixer, that automatically fixes issues found in related analysis in exakat..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Phpcsfixer
	:twitter:description: Phpcsfixer: The Phpcsfixer report provides a configuration file for php-cs-fixer, that automatically fixes issues found in related analysis in exakat.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Phpcsfixer
	:og:type: article
	:og:description: The Phpcsfixer report provides a configuration file for php-cs-fixer, that automatically fixes issues found in related analysis in exakat.
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Reports/.html
	:og:locale: en

The Phpcsfixer report provides a configuration file for php-cs-fixer, that automatically fixes issues found in related analysis in exakat.

This report builds a configuration file for php-cs-fixer. 


+ :ref:`use-===-null`  : **is_null**
+ :ref:`else-if-versus-elseif`  : **elseif**
+ :ref:`multiple-unset()`  : **combine_consecutive_unsets**
+ Classes/DontUnsetProperties: **no_unset_on_property**
+ :ref:`use-constant-instead-of-function`  : **function_to_constant**
+ :ref:`php7-dirname`  : **combine_nested_dirname**
+ :ref:`could-use-\_\_dir\_\_`  : **dir_constant**
+ :ref:`isset-multiple-arguments`  : **combine_consecutive_issets**
+ :ref:`logical-should-use-symbolic-operators`  : **logical_operators**
+ :ref:`not-not`  : **no_short_bool_cast**


`PHP-cs-fixer <https://github.com/FriendsOfPHP/PHP-CS-Fixer>`_ is a tool to automatically fix PHP Coding Standards issues. Some of the modifications are more than purely coding standards, such has replacing ``dirname(dirname($path))`` with ``dirname($path, 2)``. 

Exakat builds a configuration file for php-cs-fixer, that will automatically fix a number of results from the audit. Here is the process : 

+ Run exakat audit
+ Get Phpcsfixer report from exakat : ``php exakat.phar report -p <project> -format Phpcsfixer``
+ Update the target repository in the generated code
+ Save this new configuration in a file called '.php_cs'
+ Run php-cs-fixer on your code : ``php php-cs-fixer.phar fix /path/to/code --dry-run``
+ Fixed your code with php-cs-fixer : ``php php-cs-fixer.phar fix /path/to/code``
+ Run a new exakat audit

This configuration file should be reviewed before being used. In particular, the target files should be updated with the actual repository : this is the first part of the configuration. 

It is also recommended to use the option '--dry-run' with php-cs-fixer to check the first run. 

Php-cs-fixer runs fixes for coding standards : this reports focuses on potential fixes. It is recommended to complete this base report with extra coding conventions fixes. The building of a coding convention is outside the scope of this report. 

Exakat may find different issues than php-cs-fixer : using this report reduces the number of reported issues, but may leave some issues unsolved. In that case, manual fixing is recommended.


Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | Phpcsfixer                                                       |
+--------------+------------------------------------------------------------------+
| Rulesets     | php-cs-fixable.                                                  |
+--------------+------------------------------------------------------------------+
| Type         | JSON                                                             |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'phpcsfixer.exakat.php'.               |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


