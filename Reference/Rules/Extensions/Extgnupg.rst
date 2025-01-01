.. _extensions-extgnupg:

.. _ext-gnupgp:

ext/gnupgp
++++++++++

.. meta::
	:description:
		ext/gnupgp: Extension GnuPG.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/gnupgp
	:twitter:description: ext/gnupgp: Extension GnuPG
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/gnupgp
	:og:type: article
	:og:description: Extension GnuPG
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extgnupg.html
	:og:locale: en
Extension GnuPG.

This module allows you to interact with gnupg.

.. code-block:: php
   
   <?php
   // init gnupg
   $res = gnupg_init();
   // not really needed. Clearsign is default
   gnupg_setsignmode($res,GNUPG_SIG_MODE_CLEAR);
   // add key with passphrase 'test' for signing
   gnupg_addsignkey($res,"8660281B6051D071D94B5B230549F9DC851566DC","test");
   // sign
   $signed = gnupg_sign($res,"just a test");
   echo $signed;
   ?>

See also `Gnupg Function for PHP <http://www.php.net/manual/en/book.gnupg.php>`_ and `GnuPG <https://www.gnupg.org/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extgnupg                                                                                                                                                                     |
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


