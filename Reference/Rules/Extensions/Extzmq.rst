.. _extensions-extzmq:

.. _ext-0mq:

ext/0mq
+++++++

  Extension ext/zmq for ``0mq``.

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
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
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


