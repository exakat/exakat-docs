.. _php-password55:

.. _use-password\_hash():

Use password_hash()
+++++++++++++++++++

  `password_hash() <https://www.php.net/password_hash>`_ and password_check() are a better choice to replace the use of `crypt() <https://www.php.net/crypt>`_ to check password.

PHP 5.5 introduced these functions.


.. code-block:: php
   
   <?php
   
   $password = 'rasmuslerdorf';
   $hash = '$2y$10$YCFsG6elYca568hBi2pZ0.3LDL5wjgxct1N8w/oLR/jfHsiQwCqTS';
   
   // The cost parameter can change over time as hardware improves
   $options = array('cost' => 11);
   
   // Verify stored hash against plain-text password
   if (password_verify($password, $hash)) {
       // Check if a newer hashing algorithm is available
       // or the cost has changed
       if (password_needs_rehash($hash, PASSWORD_DEFAULT, $options)) {
           // If so, create a new hash, and replace the old one
           $newHash = password_hash($password, PASSWORD_DEFAULT, $options);
       }
   
       // Log user in
   }
   ?>

See also `Password hashing <https://www.php.net/manual/en/book.password.php>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Password55                                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.5 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


