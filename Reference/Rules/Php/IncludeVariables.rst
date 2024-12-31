.. _php-includevariables:

.. _include-variables:

Include Variables
+++++++++++++++++

.. meta\:\:
	:description:
		Include Variables: This rule reports when ``include``, ``require`` and its cousins, are used with a variable, or any data container.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Include Variables
	:twitter:description: Include Variables: This rule reports when ``include``, ``require`` and its cousins, are used with a variable, or any data container
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Include Variables
	:og:type: article
	:og:description: This rule reports when ``include``, ``require`` and its cousins, are used with a variable, or any data container
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/IncludeVariables.html
	:og:locale: en
  This rule reports when ``include``, ``require`` and its cousins, are used with a variable, or any data container. This is a dynamic inclusion.

.. code-block:: php
   
   <?php
   
   include $fileToPath;
   
   ?>
Connex PHP features
-------------------

  + `include <https://php-dictionary.readthedocs.io/en/latest/dictionary/include.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/IncludeVariables                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Dump <ruleset-Dump>`                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


