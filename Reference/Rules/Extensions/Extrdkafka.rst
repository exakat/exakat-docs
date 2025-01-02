.. _extensions-extrdkafka:

.. _ext-rdkafka:

ext/rdkafka
+++++++++++

.. meta::
	:description:
		ext/rdkafka: Extension for RDkafka.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/rdkafka
	:twitter:description: ext/rdkafka: Extension for RDkafka
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/rdkafka
	:og:type: article
	:og:description: Extension for RDkafka
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/rdkafka.html
	:og:locale: en
Extension for RDkafka.

PHP-rdkafka is a thin librdkafka binding providing a working PHP 5 / PHP 7 Kafka 0.8 / 0.9 / 0.10 client.

.. code-block:: php
   
   <?php
   
   $rk = new RdKafka\Producer();
   $rk->setLogLevel(LOG_DEBUG);
   $rk->addBrokers("10.0.0.1,10.0.0.2");
   
   ?>

See also `Kafka client for PHP <https://github.com/arnaud-lb/php-rdkafka>`_ and `librdkafka <https://github.com/edenhill/librdkafka>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extrdkafka                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.8                                                                                                                                                                                  |
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


