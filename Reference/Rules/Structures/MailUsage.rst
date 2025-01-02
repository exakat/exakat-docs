.. _structures-mailusage:

.. _mail-usage:

Mail Usage
++++++++++

.. meta::
	:description:
		Mail Usage: Report usage of mail from PHP.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Mail Usage
	:twitter:description: Mail Usage: Report usage of mail from PHP
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Mail Usage
	:og:type: article
	:og:description: Report usage of mail from PHP
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Mail Usage.html
	:og:locale: en
Report usage of mail from PHP. 

The analysis is based on `mail() <https://www.php.net/mail>`_ function and various classes used to send mail.

.. code-block:: php
   
   <?php
   // The message
   $message = "Line 1\r\nLine 2\r\nLine 3"; 
   
   // In case any of our lines are larger than 70 characters, we should use wordwrap\(\)
   $message = wordwrap($message, 70, "\r\n");
   
   // Send
   mail('caffeinated@example.com', 'My Subject', $message);
   ?>

See also `mail <https://www.php.net/mail>`_.

Connex PHP features
-------------------

  + `mail <https://php-dictionary.readthedocs.io/en/latest/dictionary/mail.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MailUsage                                                                                                                                                                    |
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


