.. _extensions-extob:

.. _ext-ob:

ext/ob
++++++

.. meta\:\:
	:description:
		ext/ob: Extension Output Buffering Control.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/ob
	:twitter:description: ext/ob: Extension Output Buffering Control
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/ob
	:og:type: article
	:og:description: Extension Output Buffering Control
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extob.html
	:og:locale: en
  Extension Output Buffering Control.

The Output Control functions allow you to control when output is sent from the script.

.. code-block:: php
   
   <?php
   
   ob_start();
   echo "Hello\n";
   
   setcookie("cookiename", "cookiedata");
   
   ob_end_flush();
   
   ?>

See also `Output Buffering Control <https://www.php.net/manual/en/book.outcontrol.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extob                                                                                                                                                                        |
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


