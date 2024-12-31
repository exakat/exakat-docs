.. _extensions-extpassword:

.. _ext-password:

ext/password
++++++++++++

.. meta\:\:
	:description:
		ext/password: Extension password.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/password
	:twitter:description: ext/password: Extension password
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/password
	:og:type: article
	:og:description: Extension password
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extpassword.html
	:og:locale: en
  Extension password.

The password hashing API provides an easy to use wrapper around `crypt() <https://www.php.net/crypt>`_ and some other password hashing algorithms, to make it easy to create and manage passwords in a `secure <https://www.php.net/secure>`_ manner.

.. code-block:: php
   
   <?php
   // See the password_hash() example to see where this came from.
   $hash = '$2y$07$BCryptRequires22Chrcte/VlQH0piJtjXl.0t1XkA8pw9dMXTpOq';
   
   if (password_verify('rasmuslerdorf', $hash)) {
       echo 'Password is valid!';
   } else {
       echo 'Invalid password.';
   }
   ?>

See also `Password Hashing <https://www.php.net/manual/en/book.password.php>`_ and `crypt man page <http://man7.org/linux/man-pages/man3/crypt.3.html>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extpassword                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


