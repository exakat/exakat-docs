.. _portability-iconvtranslit:

.. _iconv-with-translit:

Iconv With Translit
+++++++++++++++++++

.. meta::
	:description:
		Iconv With Translit: The transliteration feature of iconv() depends on the underlying system to support it.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Iconv With Translit
	:twitter:description: Iconv With Translit: The transliteration feature of iconv() depends on the underlying system to support it
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Iconv With Translit
	:og:type: article
	:og:description: The transliteration feature of iconv() depends on the underlying system to support it
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Portability/IconvTranslit.html
	:og:locale: en
The transliteration feature of `iconv() <https://www.php.net/iconv>`_ depends on the underlying system to support it. This feature is also a portability issue.

.. code-block:: php
   
   <?php
   
   $string = iconv('utf-8', 'utf-8//TRANSLIT', $source);
   
   ?>

See also `iconv() <https://www.php.net/manual/en/function.iconv.php>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/iconv%28%29%3A+Wrong+charset%2C+conversion+from+%60UTF-8%27+to+%60ASCII%2F%2FTRANSLIT%27+is+not+allowed.html>`_



Connex PHP features
-------------------

  + `iconv <https://php-dictionary.readthedocs.io/en/latest/dictionary/iconv.ini.html>`_


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


