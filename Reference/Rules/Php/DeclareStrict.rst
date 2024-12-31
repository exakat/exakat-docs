.. _php-declarestrict:

.. _strict\_types-preference:

strict_types Preference
+++++++++++++++++++++++

.. meta\:\:
	:description:
		strict_types Preference: ``strict_types`` is a PHP mode where typehint are enforced strictly or weakly.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: strict_types Preference
	:twitter:description: strict_types Preference: ``strict_types`` is a PHP mode where typehint are enforced strictly or weakly
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: strict_types Preference
	:og:type: article
	:og:description: ``strict_types`` is a PHP mode where typehint are enforced strictly or weakly
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/DeclareStrict.html
	:og:locale: en
  ``strict_types`` is a PHP mode where typehint are enforced strictly or weakly. By default, it is weak typing, allowing backward compatibility with previous versions. 

This analysis reports if ``strict_types`` are used systematically or not. ``strict_types`` affects the calling file, not the definition file.

.. code-block:: php
   
   <?php
   
   // define strict_types
   declare(strict_types = 1);
   
   foo(1);
   
   ?>

See also `Strict typing <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration.strict>`_.

Connex PHP features
-------------------

  + `strict_types <https://php-dictionary.readthedocs.io/en/latest/dictionary/strict_types.ini.html>`_


Suggestions
___________

* Use ``strict_types`` as early as possible in the development, to make it easier to adopt




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/DeclareStrict                                                                                                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.2                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


