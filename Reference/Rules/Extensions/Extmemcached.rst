.. _extensions-extmemcached:

.. _ext-memcached:

ext/memcached
+++++++++++++

.. meta::
	:description:
		ext/memcached: Extension ext-memcached.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/memcached
	:twitter:description: ext/memcached: Extension ext-memcached
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/memcached
	:og:type: article
	:og:description: Extension ext-memcached
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/memcached.html
	:og:locale: en
Extension ext-memcached.

This extension uses the libmemcached library to provide an API for communicating with memcached servers. It also provides a session handler (`memcached`).

.. code-block:: php
   
   <?php
   $m = new Memcached();
   $m->addServer('localhost', 11211);
   
   $m->set('foo', 100);
   var_dump($m->get('foo'));
   ?>

See also `ext/memcached manual <https://www.php.net/manual/en/book.memcached.php>`_ and `memcached <http://www.memcached.org/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extmemcached                                                                                                                                                                 |
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


