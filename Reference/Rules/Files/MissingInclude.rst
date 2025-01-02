.. _files-missinginclude:

.. _missing-include:

Missing Include
+++++++++++++++

.. meta::
	:description:
		Missing Include: The included files doesn't exists in the repository.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Missing Include
	:twitter:description: Missing Include: The included files doesn't exists in the repository
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Missing Include
	:og:type: article
	:og:description: The included files doesn't exists in the repository
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Missing Include.html
	:og:locale: en
The included files doesn't exists in the repository. The inclusions target a files that doesn't exist.

The analysis works with every type of inclusion : include(), require(), include_once() and require_once(). It also works with parenthesis when used as parameter delimiter.

The analysis doesn't take into account ``include_path``. This may yield false positives.
Missing included files may lead to a fatal `error <https://www.php.net/error>`_, a warning or other `error <https://www.php.net/error>`_ later in the execution.

.. code-block:: php
   
   <?php
   
   include 'non_existent.php';
   
   // variables are not resolved. This won't be reported.
   require ($path.'non_existent.php');
   
   ?>

+---------------------------+---------+---------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Name                      | Default | Type    | Description                                                                                                                                                                                                                                                                                                                                                                              |
+---------------------------+---------+---------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| constant_or_variable_name | 100     | integer | Literal value to be used when including files. For example, by configuring 'Files_MissingInclude[HOME_DIR] = /tmp/myDir/;', then 'include HOME_DIR . my_class.php; will be actually be used as '/tmp/myDir/my_class.php'. Constants must be configured with their correct case. Variable must be configured with their initial '$'. Configure any number of variable and constant names. |
+---------------------------+---------+---------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


Connex PHP features
-------------------

  + `include <https://php-dictionary.readthedocs.io/en/latest/dictionary/include.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Files/MissingInclude                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


