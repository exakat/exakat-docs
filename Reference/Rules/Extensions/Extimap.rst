.. _extensions-extimap:

.. _ext-imap:

ext/imap
++++++++

.. meta::
	:description:
		ext/imap: Extension ext/imap.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/imap
	:twitter:description: ext/imap: Extension ext/imap
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/imap
	:og:type: article
	:og:description: Extension ext/imap
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/imap.html
	:og:locale: en
Extension ext/imap.

This extension operate with the IMAP protocol, as well as the NNTP, POP3 and local mailbox access methods.

.. code-block:: php
   
   <?php
   $mbox = imap_open('{imap.example.org}', 'username', 'password', OP_HALFOPEN)
         or die('can't connect: ' . imap_last_error());
   
   $list = imap_list($mbox, '{imap.example.org}', '*');
   if (is_array($list)) {
       foreach ($list as $val) {
           echo imap_utf7_decode($val) . PHP_EOL;
       }
   } else {
       echo 'imap_list failed: ' . imap_last_error() . PHP_EOL;
   }
   
   imap_close($mbox);
   ?>

See also `IMAP <http://www.php.net/imap>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extimap                                                                                                                                                                      |
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


