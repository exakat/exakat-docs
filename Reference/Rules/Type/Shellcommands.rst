.. _type-shellcommands:

.. _shell-commands:

Shell commands
++++++++++++++

  Shell commands, called from PHP. 

Shell commands are detected with the italic quotes, and using `shell_exec() <https://www.php.net/shell_exec>`_, `system() <https://www.php.net/system>`_, `exec() <https://www.php.net/exec>`_ and `proc_open() <https://www.php.net/proc_open>`_.

.. code-block:: php
   
   <?php
   
   // Shell command in a shell_exec() call
   shell_exec('ls -1');
   
   // Shell command with backtick operator
   `ls -1 $path`;
   
   ?>

See also `Execution operator <https://www.php.net/manual/en/language.operators.execution.php>`_, `shell_exec <https://www.php.net/manual/en/function.shell-exec.php>`_ and `exec <https://www.php.net/manual/en/function.exec.php>`_.

Connex PHP features
-------------------

  + `system-call <https://php-dictionary.readthedocs.io/en/latest/dictionary/system-call.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/Shellcommands                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.9                                                                                                                                                                                   |
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


