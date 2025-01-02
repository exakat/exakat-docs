.. _extensions-extswoole:

.. _swoole:

Swoole
++++++

.. meta::
	:description:
		Swoole: Swoole : Production-Grade Async programming Framework for PHP.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Swoole
	:twitter:description: Swoole: Swoole : Production-Grade Async programming Framework for PHP
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Swoole
	:og:type: article
	:og:description: Swoole : Production-Grade Async programming Framework for PHP
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Swoole.html
	:og:locale: en
Swoole : Production-Grade Async programming Framework for PHP.

Swoole is an event-driven asynchronous & concurrent networking communication framework with high performance written only in C for PHP.

.. code-block:: php
   
   <?php
   for($i = 0; $i < 100; $i++) {
       Swoole\Coroutine::create(function() use ($i) {
           $redis = new Swoole\Coroutine\Redis();
           $res = $redis->connect('127.0.0.1', 6379);
           $ret = $redis->incr('coroutine');
           $redis->close();
           if ($i == 50) {
               Swoole\Coroutine::create(function() use ($i) {
                   $redis = new Swoole\Coroutine\Redis();
                   $res = $redis->connect('127.0.0.1', 6379);
                   $ret = $redis->set('coroutine_i', 50);
                   $redis->close();
               });
           }
       });
   }
   
   ?>

See also `Swoole <https://www.swoole.com/>`_ and `Swoole src <https://github.com/swoole/swoole-src>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extswoole                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.0                                                                                                                                                                                  |
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


