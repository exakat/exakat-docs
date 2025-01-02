.. _structures-exitusage:

.. _exit()-usage:

Exit() Usage
++++++++++++

.. meta::
	:description:
		Exit() Usage: Using exit or die() in the code makes the code untestable (it will break unit tests).
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Exit() Usage
	:twitter:description: Exit() Usage: Using exit or die() in the code makes the code untestable (it will break unit tests)
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Exit() Usage
	:og:type: article
	:og:description: Using exit or die() in the code makes the code untestable (it will break unit tests)
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Exit() Usage.html
	:og:locale: en
Using `exit <https://www.www.php.net/exit>`_ or `die() <https://www.php.net/die>`_ in the code makes the code untestable (it will `break <https://www.php.net/manual/en/control-structures.break.php>`_ unit tests). Moreover, if there is no reason or string to display, it may take a long time to spot where the application is stuck. 
Try exiting the function/class with return, or throw `exception <https://www.php.net/exception>`_ that may be caught later in the code.

.. code-block:: php
   
   <?php
   
   // Throw an exception, that may be caught somewhere
   throw new Exception('error');
   
   // Dying with error message. 
   die('error');
   
   function foo() {
       //exiting the function but not dying
       if (somethingWrong()) {
           return true;
       }
   }
   ?>
Connex PHP features
-------------------

  + `exit <https://php-dictionary.readthedocs.io/en/latest/dictionary/exit.ini.html>`_


Suggestions
___________

* Avoid exit and die. Let the script finish.
* Throw an exception and let it be handled before finishing




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ExitUsage                                                                                                                                                                                           |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-exit <https://github.com/dseguy/clearPHP/tree/master/rules/no-exit.md>`__                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-traq-structures-exitusage`, :ref:`case-thinkphp-structures-exitusage`                                                                                                                               |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


