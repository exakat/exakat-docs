.. _portability-iconvtranslit:

.. _iconv-with-translit:

Iconv With Translit
+++++++++++++++++++

.. meta::
	:description:
		Iconv With Translit: The transliteration feature of iconv() depends on the underlying operating system to support it.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Iconv With Translit
	:twitter:description: Iconv With Translit: The transliteration feature of iconv() depends on the underlying operating system to support it
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Iconv With Translit
	:og:type: article
	:og:description: The transliteration feature of iconv() depends on the underlying operating system to support it
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Iconv With Translit.html
	:og:locale: en
The transliteration feature of `iconv() <https://www.php.net/iconv>`_ depends on the underlying operating system to support it. 

Sometimes, the operating system doesn't have the needed dataset to do the conversion, and produces this `error <https://www.php.net/error>`_.

This feature is also a portability issue.

.. code-block:: php
   
   <?php
   
   $string = iconv('utf-8', 'utf-8//TRANSLIT', $source);
   
   ?>

See also `iconv() <https://www.php.net/manual/en/function.iconv.php>`_.

Related PHP errors 
-------------------

  + `iconv(): Wrong charset, conversion from `UTF-8' to `ASCII//TRANSLIT' is not allowed <https://php-errors.readthedocs.io/en/latest/messages/wrong-encoding%2C-conversion-from-%22%25s%22-to-%22%25s%22-is-not-allowed.html>`_



Connex PHP features
-------------------

  + `iconv <https://php-dictionary.readthedocs.io/en/latest/dictionary/iconv.ini.html>`_
  + `encoding <https://php-dictionary.readthedocs.io/en/latest/dictionary/encoding.ini.html>`_


Suggestions
___________

* Use an OS that supports TRANSLIT with iconv
* Remove the usage of TRANSLIT




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Portability/IconvTranslit                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


