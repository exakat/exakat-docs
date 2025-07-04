.. _extensions-extamqp:


.. _ext-amqp:

ext/amqp
++++++++

.. meta::
	:description:
		ext/amqp: Extension ``amqp``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/amqp
	:twitter:description: ext/amqp: Extension ``amqp``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/amqp
	:og:type: article
	:og:description: Extension ``amqp``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/amqp.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extamqp.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extamqp.html","name":"ext\/amqp","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension ``amqp``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/amqp.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension ``amqp``.

`PHP AMQP Binding Library`. This is an interface with the `RabbitMQ AMQP client library <https://github.`com <https://www.php.net/com>`_/alanxz/rabbitmq-c>`_. It is a  C language AMQP client library for use with version 2.0 and more recent of the ``RabbitMQ`` broker.

.. code-block:: php
   
   <?php
   $cnn = new AMQPConnection();
   $cnn->connect();
   echo 'Used channels: ', $cnn->getUsedChannels(), PHP_EOL;
   $ch = new AMQPChannel($cnn);
   echo 'Used channels: ', $cnn->getUsedChannels(), PHP_EOL;
   $ch = new AMQPChannel($cnn);
   echo 'Used channels: ', $cnn->getUsedChannels(), PHP_EOL;
   $ch = null;
   echo 'Used channels: ', $cnn->getUsedChannels(), PHP_EOL;
   ?>

See also `PHP AMQP Binding Library <https://github.com/pdezwart/php-amqp>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extamqp                                                                                                                                                                      |
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


