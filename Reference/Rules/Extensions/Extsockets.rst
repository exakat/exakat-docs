.. _extensions-extsockets:

.. _ext-sockets:

ext/sockets
+++++++++++

.. meta::
	:description:
		ext/sockets: Extension socket.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/sockets
	:twitter:description: ext/sockets: Extension socket
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/sockets
	:og:type: article
	:og:description: Extension socket
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/sockets.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extsockets.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extsockets.html","name":"ext\/sockets","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension socket","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/sockets.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Extension `socket <https://www.php.net/socket>`_.

The `socket <https://www.php.net/socket>`_ extension implements a low-level interface to the `socket <https://www.php.net/socket>`_ communication functions based on the popular BSD sockets, providing the possibility to act as a `socket <https://www.php.net/socket>`_ server as well as a client.

.. code-block:: php
   
   <?php
   
   //Example #2 Socket example: Simple TCP/IP client
   //From the PHP manual
   
   error_reporting(E_ALL);
   
   echo "<h2>TCP/IP Connection</h2>\n";
   
   /* Get the port for the WWW service. */
   $service_port = getservbyname('www', 'tcp');
   
   /* Get the IP address for the target host. */
   $address = gethostbyname('www.example.com');
   
   /* Create a TCP/IP socket. */
   $socket = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);
   if ($socket === false) {
       echo 'socket_create() failed: reason: ' . socket_strerror(socket_last_error()) . PHP_EOL;
   } else {
       echo 'OK.'.PHP_EOL;
   }
   
   echo 'Attempting to connect to '$address' on port '$service_port'...';
   $result = socket_connect($socket, $address, $service_port);
   if ($result === false) {
       echo 'socket_connect() failed.\nReason: ($result) ' . socket_strerror(socket_last_error($socket)) . '\n';
   } else {
       echo 'OK.'.PHP_EOL;
   }
   
   $in = "HEAD / HTTP/1.1\r\n";
   $in .= "Host: www.example.com\r\n";
   $in .= "Connection: Close\r\n\r\n";
   $out = '';
   
   echo 'Sending HTTP HEAD request...';
   socket_write($socket, $in, strlen($in));
   echo "OK.\n";
   
   echo 'Reading response:\n\n';
   while ($out = socket_read($socket, 2048)) {
       echo $out;
   }
   
   echo 'Closing socket...';
   socket_close($socket);
   echo 'OK.\n\n';
   ?>

See also `Sockets <https://www.php.net/manual/en/book.sockets.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extsockets                                                                                                                                                                   |
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


