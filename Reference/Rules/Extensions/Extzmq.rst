.. _extensions-extzmq:

.. _ext-0mq:

ext/0mq
+++++++

.. meta::
	:description:
		ext/0mq: Extension ext/zmq for ``0mq``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/0mq
	:twitter:description: ext/0mq: Extension ext/zmq for ``0mq``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/0mq
	:og:type: article
	:og:description: Extension ext/zmq for ``0mq``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/0mq.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extzmq.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extzmq.html","name":"ext\/0mq","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension ext\/zmq for ``0mq``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/0mq.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Extension ext/zmq for ``0mq``.

``ØMQ is a software library that lets you quickly design and implement a fast message-based application.``

.. code-block:: php
   
   <?php
   
   // Example from https://github.com/kuying/ZeroMQ/blob/d80dcc3dc1c14a343ca90bbd656b98fd55366548/zguide/examples/PHP/msgqueue.php
       /*
        *  Simple message queuing broker
        *  Same as request-reply broker but using QUEUE device
        * @author Ian Barber <ian(dot)barber(at)gmail(dot)com>
        */
       $context = new ZMQContext();
       //  Socket facing clients
       $frontend = $context->getSocket(ZMQ::SOCKET_ROUTER);
       $frontend->bind("tcp://*:5559");
       //  Socket facing services
       $backend = $context->getSocket(ZMQ::SOCKET_DEALER);
       $backend->bind("tcp://*:5560");
       //  Start built-in device
       new ZMQDevice($frontend, $backend);
   
   ?>

See also `ZeroMQ <http://zeromq.org/>`_ and `ZMQ <https://www.php.net/manual/en/book.zmq.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extzmq                                                                                                                                                                       |
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


