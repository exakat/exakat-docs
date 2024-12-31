.. _extensions-exttrader:

.. _ext-trader:

ext/trader
++++++++++

.. meta\:\:
	:description:
		ext/trader: Extension trader.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/trader
	:twitter:description: ext/trader: Extension trader
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/trader
	:og:type: article
	:og:description: Extension trader
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Exttrader.html
	:og:locale: en
  Extension trader.

The trader extension is a free open source stock library based on TA-Lib. It's dedicated to trading software developers requiring to perform technical analysis of financial market data.

.. code-block:: php
   
   <?php
   
   // get_data() reads the data from a source 
   var_dump(trader_avgprice(
   	get_data("open", $data0),
   	get_data("high", $data0),
   	get_data("low", $data0),
   	get_data("close", $data0)
   ));
   
   ?>

See also `trader (PECL) <https://pecl.php.net/package/trader>`_, 'TA-lib <http://www.ta-lib.org/>`_ and `ext/trader <https://www.php.net/manual/en/book.trader.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Exttrader                                                                                                                                                                    |
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


