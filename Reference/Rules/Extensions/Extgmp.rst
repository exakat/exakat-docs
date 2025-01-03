.. _extensions-extgmp:

.. _ext-gmp:

ext/gmp
+++++++

.. meta::
	:description:
		ext/gmp: Extension ext/gmp.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/gmp
	:twitter:description: ext/gmp: Extension ext/gmp
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/gmp
	:og:type: article
	:og:description: Extension ext/gmp
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/gmp.html
	:og:locale: en
Extension ext/`gmp <https://www.php.net/gmp>`_.

These functions allow for arbitrary-length integers to be worked with using the GNU MP library.

.. code-block:: php
   
   <?php
   $pow1 = gmp_pow('2', 131);
   echo gmp_strval($pow1) . PHP_EOL;
   $pow2 = gmp_pow('0', 0);
   echo gmp_strval($pow2) . PHP_EOL;
   $pow3 = gmp_pow('2', -1); // Negative exp, generates warning
   echo gmp_strval($pow3) . PHP_EOL;
   ?>

See also `GMP <https://www.php.net/manual/en/book.gmp.php>`_ and `GNU MP library <https://gmplib.org/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extgmp                                                                                                                                                                       |
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


