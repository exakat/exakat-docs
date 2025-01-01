.. _extensions-extmailparse:

.. _ext-mailparse:

ext/mailparse
+++++++++++++

.. meta::
	:description:
		ext/mailparse: Extension mailparse.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/mailparse
	:twitter:description: ext/mailparse: Extension mailparse
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/mailparse
	:og:type: article
	:og:description: Extension mailparse
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extmailparse.html
	:og:locale: en
Extension mailparse.

Mailparse is an extension for parsing and working with email messages. It can deal with `RFC 822 (MIME) <http://www.faqs.org/rfcs/rfc822.html>`_ and `RFC 2045 (MIME) <http://www.faqs.org/rfcs/rfc2045.html>`_ compliant messages.

.. code-block:: php
   
   <?php
   
   $mail = mailparse_msg_create();
   mailparse_msg_parse($mail, $mailInString);
   $parts = mailparse_msg_get_structure($mail); 
   
   foreach($parts as $part) { 
       $section = mailparse_msg_get_part($mail, $part); 
       $info = mailparse_msg_get_part_data($section); 
   }
   
   ?>

See also `Mailparse <https://www.php.net/manual/en/book.mailparse.php>`_.

Connex PHP features
-------------------

  + `email <https://php-dictionary.readthedocs.io/en/latest/dictionary/email.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extmailparse                                                                                                                                                                 |
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


