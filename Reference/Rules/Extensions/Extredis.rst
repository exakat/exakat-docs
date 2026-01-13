.. _extensions-extredis:

.. _ext-redis:

ext/redis
+++++++++

  Extension ext/redis.

The phpredis extension provides an API for communicating with the Redis key-value store.

.. code-block:: php
   
   <?php
   
   $redis = new Redis();
   $redis->connect('127.0.0.1', 6379);
   
   $redis->setOption(Redis::OPT_SERIALIZER, Redis::SERIALIZER_NONE);	// don't serialize data
   $redis->setOption(Redis::OPT_SERIALIZER, Redis::SERIALIZER_PHP);	// use built-in serialize/unserialize
   $redis->setOption(Redis::OPT_SERIALIZER, Redis::SERIALIZER_IGBINARY);	// use igBinary serialize/unserialize
   
   $redis->setOption(Redis::OPT_PREFIX, 'myAppName:');	// use custom prefix on all keys
   
   /* Options for the SCAN family of commands, indicating whether to abstract
      empty results from the user.  If set to SCAN_NORETRY (the default), phpredis
      will just issue one SCAN command at a time, sometimes returning an empty
      array of results.  If set to SCAN_RETRY, phpredis will retry the scan command
      until keys come back OR Redis returns an iterator of zero
   */
   $redis->setOption(Redis::OPT_SCAN, Redis::SCAN_NORETRY);
   $redis->setOption(Redis::OPT_SCAN, Redis::SCAN_RETRY);
   ?>

See also `A PHP extension for Redis <https://github.com/phpredis/phpredis/>`_ and `Redis <https://redis.io/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extredis                                                                                                                                                                     |
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


