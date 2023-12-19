.. _php-usesessionstartoptions:

.. _use-session\_start()-options:

Use session_start() Options
+++++++++++++++++++++++++++

  It is possible to set the session's option at `session_start() <https://www.php.net/session_start>`_ call, skipping the usage of session_option().

This way, session's options are set in one call, saving several hits.

This is available since PHP 7.0. It is recommended to set those values in the ``php.ini`` file, whenever possible. 


.. code-block:: php
   
   <?php
   
   // PHP 7.0
   session_start(['session.name' => 'mySession',
                  'session.cookie_httponly' => 1,
                  'session.gc_maxlifetime' => 60 * 60);
   
   // PHP 5.6- old way 
   ini_set ('session.name', 'mySession');
   ini_set("session.cookie_httponly", 1); 
   ini_set('session.gc_maxlifetime', 60 * 60);
   session_start();
   
   ?>

Suggestions
___________

* Use session_start() with array arguments




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseSessionStartOptions                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.8                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | session                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-php-usesessionstartoptions`                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


