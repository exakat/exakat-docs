.. _security-cantdisablefunction:

.. _can't-disable-function:

Can't Disable Function
++++++++++++++++++++++

  This is the list of potentially dangerous PHP functions being used in the code, such as `exec() <https://www.php.net/exec>`_ or `fsockopen() <https://www.php.net/fsockopen>`_. 

eval() is not reported here, as it is not a PHP function, but a language construct : it can't be disabled.
This analysis is the base for suggesting values for the ``disable_functions`` directive.

.. code-block:: php
   
   <?php
   
   // This script uses ftp_connect(), therefore, this function shouldn't be disabled. 
   $ftp = ftp_connect($host, 21);
   
   // This script doesn't use imap_open(), therefore, this function may be disabled. 
   
   ?>
Connex PHP features
-------------------

  + `disable-functions <https://php-dictionary.readthedocs.io/en/latest/dictionary/disable-functions.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/CantDisableFunction                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`can't-disable-class`                                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


