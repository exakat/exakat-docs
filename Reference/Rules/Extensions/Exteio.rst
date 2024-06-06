.. _extensions-exteio:

.. _ext-eio:

ext/eio
+++++++

  Extension EIO.

This is a PHP extension wrapping functions of the `libeio <http://software.schmorp.de/pkg/libeio.html>`_ library written by Marc Lehmann.

Libeio is a an asynchronous I/O library. Features basically include asynchronous versions of POSIX API(read, write, open, close, stat, unlink, fdatasync, mknod, readdir etc.); sendfile (native on Solaris, Linux, HP-UX, FreeBSD); readahead. libeio itself emulates the system calls, if they are not available on specific(UNIX-like) platform.

.. code-block:: php
   
   <?php
   $str      = str_repeat('1', 20);
   $filename = '/tmp/tmp_file' .uniqid();
   @unlink($filename);
   touch($filename);
   eio_open($filename, EIO_O_RDWR, NULL, EIO_PRI_DEFAULT, function($filename, $fd) use ($str) {
   	eio_write($fd, $str, strlen($str), 0, null, function($fd, $written) use ($str, $filename) {
   		var_dump([
   			'written'  => $written,
   			'strlen'   => strlen($str),
   			'filesize' => filesize($filename),
   			'count'    => substr_count(file_get_contents($filename), '1')
   			]);
   	}, $fd);
   }, $filename);
   eio_event_loop();
   ?>

See also `libeio <http://software.schmorp.de/pkg/libeio.html>`_ and `PHP extension for libeio  <https://github.com/rosmanov/pecl-eio>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Exteio                                                                                                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.3                                                                                                                                                                                   |
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


