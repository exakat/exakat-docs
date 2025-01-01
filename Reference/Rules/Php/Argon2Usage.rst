.. _php-argon2usage:

.. _argon2-usage:

Argon2 Usage
++++++++++++

.. meta::
	:description:
		Argon2 Usage: Argon2 is an optionally compiled password hashing API.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Argon2 Usage
	:twitter:description: Argon2 Usage: Argon2 is an optionally compiled password hashing API
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Argon2 Usage
	:og:type: article
	:og:description: Argon2 is an optionally compiled password hashing API
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/Argon2Usage.html
	:og:locale: en
Argon2 is an optionally compiled password hashing API. 

Argon2 has been added to the password hashing API in PHP 7.2. 

It is not available in older version. It also requires PHP to be compiled with the --with-password-argon2 option.

.. code-block:: php
   
   <?php
   
   // Hashing a password with argon2
   $hash = password_hash('password', PASSWORD_ARGON2I, ['memory_cost' => 1<<17, 
                                                        'time_cost'   => PASSWORD_ARGON2_DEFAULT_TIME_COST, 
                                                        'threads'     => PASSWORD_ARGON2_DEFAULT_THREADS]);
   
   ?>

See also `Argon2 Password Hash <https://wiki.php.net/rfc/argon2_password_hash>`_.

Connex PHP features
-------------------

  + `argon2 <https://php-dictionary.readthedocs.io/en/latest/dictionary/argon2.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Argon2Usage                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


