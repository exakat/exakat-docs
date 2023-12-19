.. _functions-hardcodedpasswords:

.. _hardcoded-passwords:

Hardcoded Passwords
+++++++++++++++++++

  Hardcoded passwords in the code. 

Hardcoding passwords is a bad idea. Not only it make the code difficult to change, but it is an information leak. It is better to hide this kind of information out of the code.


.. code-block:: php
   
   <?php
   
   $ftp_server = '300.1.2.3';   // yes, this doesn't exists, it's an example
   $conn_id = ftp_connect($ftp_server); 
   
   // login with username and password
   $login_result = ftp_login($conn_id, 'login', 'password'); 
   
   ?>

+---------------+--------------------+------+-------------------------------------------------------------------------------------------------+
| Name          | Default            | Type | Description                                                                                     |
+---------------+--------------------+------+-------------------------------------------------------------------------------------------------+
| passwordsKeys | password_keys.json | data | List of array index and property names that shall be checked for potential secret key storages. |
+---------------+--------------------+------+-------------------------------------------------------------------------------------------------+



See also `10 GitHub Security Best Practices <https://snyk.io/blog/ten-git-hub-security-best-practices/>`_ and `Git How-To: Remove Your Password from a Repository <https://davidverhasselt.com/git-how-to-remove-your-password-from-a-repository/>`_.


Suggestions
___________

* Remove all passwords from the code. Also, check for history if you are using a VCS.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/HardcodedPasswords                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Security <ruleset-Security>`                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | password, hard-coded                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-hardcoded-credential <https://github.com/dseguy/clearPHP/tree/master/rules/no-hardcoded-credential.md>`__           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


