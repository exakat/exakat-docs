.. _extensions-extapcu:

.. _ext-apcu:

ext/apcu
++++++++

.. meta::
	:description:
		ext/apcu: Extension ``APCU``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/apcu
	:twitter:description: ext/apcu: Extension ``APCU``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/apcu
	:og:type: article
	:og:description: Extension ``APCU``
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extapcu.html
	:og:locale: en
Extension ``APCU``.

``APCu`` is ``APC`` stripped of opcode caching. The Alternative PHP Cache (APC) is a free and open opcode cache for PHP. Its goal is to provide a free, open, and robust framework for caching and optimizing PHP intermediate code.

.. code-block:: php
   
   <?php
   $bar = 'BAR';
   apcu_add('foo', $bar);
   var_dump(apcu_fetch('foo'));
   echo "\n";
   $bar = 'NEVER GETS SET';
   apcu_add('foo', $bar);
   var_dump(apcu_fetch('foo'));
   echo "\n";
   ?>

See also `APCU <http://www.php.net/manual/en/book.apcu.php>`_, `ext/apcu <https://pecl.php.net/package/APCu>`_ and `krakjoe/apcu <https://github.com/krakjoe/apcu>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extapcu                                                                                                                                                                      |
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


