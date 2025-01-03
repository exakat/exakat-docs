.. _extensions-extpcov:

.. _ext-pcov:

ext/pcov
++++++++

.. meta::
	:description:
		ext/pcov: CodeCoverage compatible driver for PHP.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/pcov
	:twitter:description: ext/pcov: CodeCoverage compatible driver for PHP
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/pcov
	:og:type: article
	:og:description: CodeCoverage compatible driver for PHP
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/pcov.html
	:og:locale: en
CodeCoverage compatible driver for PHP.

A `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ contained CodeCoverage compatible driver for PHP7. CodeCoverage provides collection, processing, and rendering functionality for PHP code coverage information.

.. code-block:: php
   
   <?php
   \pcov\start();
   $d = [];
   for ($i = 0; $i < 10; $i++) {
   	$d[] = $i * 42;
   }
   \pcov\stop();
   var_dump(\pcov\collect());
   ?>

See also `PCOV <https://github.com/krakjoe/pcov>`_ and `phpunit/php-code-coverage <https://github.com/sebastianbergmann/php-code-coverage>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extpcov                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.5                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


