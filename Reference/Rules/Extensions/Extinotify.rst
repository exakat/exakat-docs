.. _extensions-extinotify:

.. _ext-inotify:

ext/inotify
+++++++++++

.. meta::
	:description:
		ext/inotify: Extension inotify.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/inotify
	:twitter:description: ext/inotify: Extension inotify
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/inotify
	:og:type: article
	:og:description: Extension inotify
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/inotify.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extinotify.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extinotify.html","name":"ext\/inotify","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension inotify","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/inotify.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Extension inotify.

The Inotify extension gives access to the Linux kernel subsystem that acts to extend filesystems to notice changes to the filesystem, and report those changes to applications.

.. code-block:: php
   
   <?php
   // Open an inotify instance
   $fd = inotify_init();
   
   // Watch __FILE__ for metadata changes (e.g. mtime)
   $watch_descriptor = inotify_add_watch($fd, __FILE__, IN_ATTRIB);
   
   // generate an event
   touch(__FILE__);
   
   // Read events
   $events = inotify_read($fd);
   print_r($events);
   
   // The following methods allows to use inotify functions without blocking on inotify_read():
   
   // - Using stream_select() on $fd:
   $read = array($fd);
   $write = null;
   $except = null;
   stream_select($read,$write,$except,0);
   
   // - Using stream_set_blocking() on $fd
   stream_set_blocking($fd, 0);
   inotify_read($fd); // Does no block, and return false if no events are pending
   
   // - Using inotify_queue_len() to check if event queue is not empty
   $queue_len = inotify_queue_len($fd); // If > 0, inotify_read() will not block
   
   // Stop watching __FILE__ for metadata changes
   inotify_rm_watch($fd, $watch_descriptor);
   
   // Close the inotify instance
   // This may have closed all watches if this was not already done
   fclose($fd);
   
   ?>

See also `ext/inotify manual <https://www.php.net/manual/en/book.inotify.php>`_ and `inotify <https://en.wikipedia.org/wiki/Inotify>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extinotify                                                                                                                                                                   |
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


