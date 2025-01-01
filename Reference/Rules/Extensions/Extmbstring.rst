.. _extensions-extmbstring:

.. _ext-mbstring:

ext/mbstring
++++++++++++

.. meta::
	:description:
		ext/mbstring: Extension ``ext/mbstring``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/mbstring
	:twitter:description: ext/mbstring: Extension ``ext/mbstring``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/mbstring
	:og:type: article
	:og:description: Extension ``ext/mbstring``
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extmbstring.html
	:og:locale: en
Extension ``ext/mbstring``.

``mbstring`` provides multibyte specific string functions that help you deal with multibyte encodings in PHP.

.. code-block:: php
   
   <?php
   /* Convert internal character encoding to SJIS */
   $str = mb_convert_encoding($str, "SJIS");
   
   /* Convert EUC-JP to UTF-7 */
   $str = mb_convert_encoding($str, "UTF-7", "EUC-JP");
   
   /* Auto detect encoding from JIS, eucjp-win, sjis-win, then convert str to UCS-2LE */
   $str = mb_convert_encoding($str, "UCS-2LE", "JIS, eucjp-win, sjis-win");
   
   /* "auto" is expanded to "ASCII,JIS,UTF-8,EUC-JP,SJIS" */
   $str = mb_convert_encoding($str, "EUC-JP", "auto");
   ?>

See also `Mbstring <http://www.php.net/manual/en/book.mbstring.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extmbstring                                                                                                                                                                  |
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


