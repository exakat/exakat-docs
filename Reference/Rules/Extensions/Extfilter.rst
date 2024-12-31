.. _extensions-extfilter:

.. _ext-filter:

ext/filter
++++++++++

.. meta\:\:
	:description:
		ext/filter: Extension filter.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/filter
	:twitter:description: ext/filter: Extension filter
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/filter
	:og:type: article
	:og:description: Extension filter
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extfilter.html
	:og:locale: en
  Extension filter.

This extension filters data by either validating or sanitizing it.

.. code-block:: php
   
   <?php
   $email_a = 'joe@example.com';
   $email_b = 'bogus';
   
   if (filter_var($email_a, FILTER_VALIDATE_EMAIL)) {
       echo 'This ($email_a) email address is considered valid.'.PHP_EOL;
   }
   if (filter_var($email_b, FILTER_VALIDATE_EMAIL)) {
       echo 'This ($email_b) email address is considered valid.'.PHP_EOL;
   } else {
       echo 'This ($email_b) email address is considered invalid.'.PHP_EOL;
   }
   ?>

See also `Data filtering <https://www.php.net/manual/en/book.filter.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extfilter                                                                                                                                                                    |
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


