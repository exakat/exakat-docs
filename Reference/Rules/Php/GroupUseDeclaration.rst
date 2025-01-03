.. _php-groupusedeclaration:

.. _group-use-declaration:

Group Use Declaration
+++++++++++++++++++++

.. meta::
	:description:
		Group Use Declaration: This rule reports when a group use declaration is used.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Group Use Declaration
	:twitter:description: Group Use Declaration: This rule reports when a group use declaration is used
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Group Use Declaration
	:og:type: article
	:og:description: This rule reports when a group use declaration is used
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Group Use Declaration.html
	:og:locale: en
This rule reports when a group use declaration is used. This is PHP feature since version 7.0, yet it is seldom used.

.. code-block:: php
   
   <?php
   
   // Adapted from the RFC documentation 
   // Pre PHP 7 code
   use some\name_space\ClassA;
   use some\name_space\ClassB;
   use some\name_space\ClassC as C;
   
   use function some\name_space\fn_a;
   use function some\name_space\fn_b;
   use function some\name_space\fn_c;
   
   use const some\name_space\ConstA;
   use const some\name_space\ConstB;
   use const some\name_space\ConstC;
   
   // PHP 7+ code
   use some\name_space\{ClassA, ClassB, ClassC as C};
   use function some\name_space\{fn_a, fn_b, fn_c};
   use const some\name_space\{ConstA, ConstB, ConstC};
   
   ?>

See also `Group Use Declaration RFC <https://wiki.php.net/rfc/group_use_declarations>`_ and `Using namespaces: Aliasing/Importing <https://www.php.net/manual/en/language.namespaces.importing.php>`_.

Connex PHP features
-------------------

  + `use <https://php-dictionary.readthedocs.io/en/latest/dictionary/use.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/GroupUseDeclaration                                                                                                                                                                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.7                                                                                                                                                                                                                                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                                                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


