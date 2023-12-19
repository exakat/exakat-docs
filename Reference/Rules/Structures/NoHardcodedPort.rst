.. _structures-nohardcodedport:

.. _no-hardcoded-port:

No Hardcoded Port
+++++++++++++++++

  When connecting to a remove server, port is an important information. It is recommended to make this configurable (with constant or configuration), to as to be able to change this value without changing the code.


.. code-block:: php
   
   <?php
   
       // Both configurable IP and hostname
       $connection = ssh2_connect($_ENV['SSH_HOST'], $_ENV['SSH_PORT'], $methods, $callbacks);
       
       // Both hardcoded IP and hostname
       $connection = ssh2_connect('shell.example.com', 22, $methods, $callbacks);
   
       if (!$connection) die('Connection failed');
   ?>

Suggestions
___________

* Move the port to a configuration file, an environment variable




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoHardcodedPort                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Security <ruleset-Security>`                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | port                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-structures-nohardcodedport`                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


