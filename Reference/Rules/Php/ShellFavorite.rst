.. _php-shellfavorite:

.. _shell-favorite:

Shell Favorite
++++++++++++++

  PHP has several syntax to make system calls : `shell_exec() <https://www.php.net/shell_exec>`_, `exec() <https://www.php.net/exec>`_ and back-ticks, &#96; are the common ones. 

It was found that one of those three is actually being used over 90% of the time. The remaining cases should be uniformed, so has to make this code consistent.


.. code-block:: php
   
   <?php
   
   // back-ticks &#96; are only used once.
   &#96;back-tick&#96;;
   
   shell_exec('exec1');
   shell_exec('exec2');
   shell_exec('exec3');
   shell_exec('exec4');
   shell_exec('exec5');
   shell_exec('exec6');
   shell_exec('exec7');
   shell_exec('exec8');
   shell_exec('exec9');
   shell_exec('exec10');
   shell_exec('exec11');
   shell_exec('exec12');
   
   ?>

See also `Execution Operators <https://www.php.net/manual/en/language.operators.execution.php>`_, `shell_exec() <https://www.php.net/shell_exec>`_ and `ptlis/shell-command <https://packagist.org/packages/ptlis/shell-command>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ShellFavorite                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Preferences <ruleset-Preferences>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.9                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | shell                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


