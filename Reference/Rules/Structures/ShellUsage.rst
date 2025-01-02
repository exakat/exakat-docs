.. _structures-shellusage:

.. _shell-usage:

Shell Usage
+++++++++++

.. meta::
	:description:
		Shell Usage: List of shell calls to system.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Shell Usage
	:twitter:description: Shell Usage: List of shell calls to system
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Shell Usage
	:og:type: article
	:og:description: List of shell calls to system
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Shell Usage.html
	:og:locale: en
List of shell calls to system.

.. code-block:: php
   
   <?php
       // Using backtick operator
       $a = `ls -hla`;
       
       // Using one of PHP native or extension functions
       $a = shell_exec('ls -hla');
       $b = \pcntl_exec('/path/to/command');
       
   ?>

See also `shell_exec <http://www.php.net/shell_exec>`_ and `Execution Operators <http://www.php.net/manual/en/language.operators.execution.php>`_.

Connex PHP features
-------------------

  + `shell <https://php-dictionary.readthedocs.io/en/latest/dictionary/shell.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ShellUsage                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


