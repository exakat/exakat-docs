.. _extensions-exticonv:

.. _ext-iconv:

ext/iconv
+++++++++

.. meta::
	:description:
		ext/iconv: Extension ext/iconv.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/iconv
	:twitter:description: ext/iconv: Extension ext/iconv
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/iconv
	:og:type: article
	:og:description: Extension ext/iconv
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/iconv.html
	:og:locale: en
Extension ext/iconv.

 With this module, you can turn a string represented by a local character set into the one represented by another character set, which may be the Unicode character set.

.. code-block:: php
   
   <?php
   $text = "This is the Euro symbol '€'.";
   
   echo 'Original : ', $text, PHP_EOL;
   echo 'TRANSLIT : ', iconv("UTF-8", "ISO-8859-1//TRANSLIT", $text), PHP_EOL;
   echo 'IGNORE   : ', iconv("UTF-8", "ISO-8859-1//IGNORE", $text), PHP_EOL;
   echo 'Plain    : ', iconv("UTF-8", "ISO-8859-1", $text), PHP_EOL;
   
   ?>

See also `Iconv <https://www.php.net/iconv>`_ and `libiconv <https://www.gnu.org/software/libiconv/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Exticonv                                                                                                                                                                     |
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


