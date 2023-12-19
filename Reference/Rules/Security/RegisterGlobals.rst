.. _security-registerglobals:

.. _register-globals:

Register Globals
++++++++++++++++

  ``register_globals`` was a PHP directive that dumped all incoming variables from GET, POST, COOKIE and FILES as global variables in the called scripts.
This lead to security failures, as the variables were often used but not filtered. 

Though it is less often found in more recent code, ``register_globals`` is sometimes needed in legacy code, that haven't made the move to eradicate this style of coding.
Backward compatible pieces of code that mimic the ``register_globals`` features usually create even greater security risks by being run after scripts startup. At that point, some important variables are already set, and may be overwritten by the incoming call, creating confusion in the script.

Mimicking ``register_globals`` is achieved with variables variables, `extract() <https://www.php.net/extract>`_, `parse_str() <https://www.php.net/parse_str>`_ and import_request_variables() (Up to PHP 5.4). 


.. code-block:: php
   
   <?php
   
   // Security warning ! This overwrites existing variables. 
   extract($_POST);
   
   // Security warning ! This overwrites existing variables. 
   foreach($_REQUEST as $var => $value) {
       $$var = $value;
   }
   
   ?>

Suggestions
___________

* Avoid implementing again ``register_globals``
* Use a container to store and access commonly used values




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/RegisterGlobals                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Security <ruleset-Security>`                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | register-globals                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-teampass-security-registerglobals`, :ref:`case-xoops-security-registerglobals`                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


