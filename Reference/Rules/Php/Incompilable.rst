.. _php-incompilable:

.. _incompilable-files:

Incompilable Files
++++++++++++++++++

.. meta\:\:
	:description:
		Incompilable Files: Files that cannot be compiled, and, as such, be run by PHP.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Incompilable Files
	:twitter:description: Incompilable Files: Files that cannot be compiled, and, as such, be run by PHP
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Incompilable Files
	:og:type: article
	:og:description: Files that cannot be compiled, and, as such, be run by PHP
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/Incompilable.html
	:og:locale: en
  Files that cannot be compiled, and, as such, be run by PHP. Scripts are linted against various versions of PHP. 

This is usually undesirable, as all code must compile before being executed. It may be that such files are not compilable because they are not yet ready for an upcoming PHP version.



Code that is not compilable with older PHP versions means that the code is breaking backward compatibility : good or bad is project decision.

When the code is used as a template for PHP code generation, for example at installation time, it is recommended to use a distinct file extension, so as to distinguish them from actual PHP code.

.. code-block:: php
   
   <?php
   
   // Can't compile this : Print only accepts one argument
   print $a, $b, $c;
   
   ?>

Suggestions
___________

* If this file is a template for PHP code, change the extension to something else than .php
* Fix the syntax so it works with various versions of PHP




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Incompilable                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-incompilable <https://github.com/dseguy/clearPHP/tree/master/rules/no-incompilable.md>`__                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-xataface-php-incompilable`                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


