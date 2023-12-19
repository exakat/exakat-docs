.. _security-nosleep:

.. _avoid-sleep()-usleep():

Avoid sleep()/usleep()
++++++++++++++++++++++

  `sleep() <https://www.php.net/sleep>`_ and `usleep() <https://www.php.net/usleep>`_ help saturate the web server. 

Pausing the script for a specific amount of time means that the Web server is also making all related resources sleep, such as database, sockets, session, etc. This may used to set up a DOS on the server.  


.. code-block:: php
   
   <?php
   
   $begin = microtime(true);
   checkLogin($user, $password);
   $end   = microtime(true);
   
   // Making all login checks looks the same
   usleep(1000000 - ($end - $begin) * 1000000); 
   
   // Any hit on this page now uses 1 second, no matter if load is high or not
   // Is it now possible to saturate the webserver in 1 s ? 
   
   ?>


As much as possible, avoid delaying the end of the script. 

`sleep() <https://www.php.net/sleep>`_ and `usleep() <https://www.php.net/usleep>`_ have less impact in commandline (``CLI``).

Suggestions
___________

* Add a deadline of usage in the session, and wait past this deadline to start serving again. Until then, abort immediately.
* Use element in the GUI to delay or slow usage.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/NoSleep                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Security <ruleset-Security>`                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | sleep, cli                                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


