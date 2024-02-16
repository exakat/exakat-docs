.. _security-mkdirdefault:

.. _mkdir-default:

Mkdir Default
+++++++++++++

  `mkdir() <https://www.php.net/mkdir>`_ gives universal access to created folders, by default. It is recommended to gives limited set of rights (0755, 0700), or to explicitly set the rights to 0777. 


.. code-block:: php
   
   <?php
   
   // By default, this dir is 777
   mkdir('/path/to/dir');
   
   // Explicitely, this is wanted. It may also be audited easily
   mkdir('/path/to/dir', 0777);
   
   // This dir is limited to the current user. 
   mkdir('/path/to/dir', 0700);
   
   ?>

See also `Why 777 Folder Permissions are a Security Risk <https://www.spiralscripts.co.uk/Blog/why-777-folder-permissions-are-a-security-risk.html>`_.


Suggestions
___________

* Always use the lowest possible privileges on folders
* Don't use the PHP default : at least, make it explicit that the 'universal' rights are voluntary




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/MkdirDefault                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Security <ruleset-Security>`                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.2                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | dir                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-mautic-security-mkdirdefault`, :ref:`case-openemr-security-mkdirdefault`                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


