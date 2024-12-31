.. _structures-nohardcodedport:

.. _no-hardcoded-port:

No Hardcoded Port
+++++++++++++++++

.. meta\:\:
	:description:
		No Hardcoded Port: When connecting to a remove server, port is an important information.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Hardcoded Port
	:twitter:description: No Hardcoded Port: When connecting to a remove server, port is an important information
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Hardcoded Port
	:og:type: article
	:og:description: When connecting to a remove server, port is an important information
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/NoHardcodedPort.html
	:og:locale: en
  When connecting to a remove server, port is an important information. It is recommended to make this configurable (with constant or configuration), to as to be able to change this value without changing the code.

.. code-block:: php
   
   <?php
   
       // Both configurable IP and hostname
       $connection = ssh2_connect($_ENV['SSH_HOST'], $_ENV['SSH_PORT'], $methods, $callbacks);
       
       // Both hardcoded IP and hostname
       $connection = ssh2_connect('shell.example.com', 22, $methods, $callbacks);
   
       if (!$connection) die('Connection failed');
   ?>
Connex PHP features
-------------------

  + `port <https://php-dictionary.readthedocs.io/en/latest/dictionary/port.ini.html>`_


Suggestions
___________

* Move the port to a configuration file, an environment variable




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoHardcodedPort                                                                                                                         |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-structures-nohardcodedport`                                                                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------+


