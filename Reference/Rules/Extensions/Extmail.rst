.. _extensions-extmail:

.. _ext-mail:

ext/mail
++++++++

.. meta\:\:
	:description:
		ext/mail: Extension for mail.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/mail
	:twitter:description: ext/mail: Extension for mail
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/mail
	:og:type: article
	:og:description: Extension for mail
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extmail.html
	:og:locale: en
  Extension for mail.

The `mail() <https://www.php.net/mail>`_ function allows you to send mail.

.. code-block:: php
   
   <?php
   // The message
   $message = "Line 1\r\nLine 2\r\nLine 3";
   
   // In case any of our lines are larger than 70 characters, we should use wordwrap()
   $message = wordwrap($message, 70, "\r\n");
   
   // Send
   mail('caffeinated@example.com', 'My Subject', $message);
   ?>

See also `Mail related functions <http://www.php.net/manual/en/book.mail.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extmail                                                                                                                                                                      |
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


