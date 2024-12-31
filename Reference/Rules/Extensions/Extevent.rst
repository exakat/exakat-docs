.. _extensions-extevent:

.. _ext-event:

ext/event
+++++++++

.. meta\:\:
	:description:
		ext/event: Extension event.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/event
	:twitter:description: ext/event: Extension event
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/event
	:og:type: article
	:og:description: Extension event
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extevent.html
	:og:locale: en
  Extension event.

This is an extension to efficiently schedule I/O, time and signal based events using the best I/O notification mechanism available for specific platform. This is a port of libevent to the PHP infrastructure.

.. code-block:: php
   
   <?php
   // Read callback
   function readcb($bev, $base) {
       //$input = $bev->input; //$bev->getInput();
   
       //$pos = $input->search('TTP');
       $pos = $bev->input->search('TTP');
   
       while (($n = $bev->input->remove($buf, 1024)) > 0) {
           echo $buf;
       }
   }
   
   // Event callback
   function eventcb($bev, $events, $base) {
       if ($events & EventBufferEvent::CONNECTED) {
           echo 'Connected.';
       } elseif ($events & (EventBufferEvent::ERROR | EventBufferEvent::EOF)) {
           if ($events & EventBufferEvent::ERROR) {
               echo 'DNS error: ', $bev->getDnsErrorString(), PHP_EOL;
           }
   
           echo 'Closing'.PHP_EOL;
           $base->exit();
           exit('Done'.PHP_EOL);
       }
   }
   
   if ($argc != 3) {
       echo <<<EOS
   Trivial HTTP 0.x client
   Syntax: php {$argv[0]} [hostname] [resource]
   Example: php {$argv[0]} www.google.com /
   
   EOS;
       exit();
   }
   
   $base = new EventBase();
   
   $dns_base = new EventDnsBase($base, TRUE); // We'll use async DNS resolving
   if (!$dns_base) {
       exit('Failed to init DNS Base'.PHP_EOL);
   }
   
   $bev = new EventBufferEvent($base, /* use internal socket */ NULL,
       EventBufferEvent::OPT_CLOSE_ON_FREE | EventBufferEvent::OPT_DEFER_CALLBACKS,
       'readcb', /* writecb */ NULL, 'eventcb'
   );
   if (!$bev) {
       exit('Failed creating bufferevent socket'.PHP_EOL);
   }
   
   //$bev->setCallbacks('readcb', /* writecb */ NULL, 'eventcb', $base);
   $bev->enable(Event::READ | Event::WRITE);
   
   $output = $bev->output; //$bev->getOutput();
   if (!$output->add(
       'GET '.$argv[2].' HTTP/1.0'."\r\n".
       'Host: '.$argv[1]."\r\n".
       'Connection: Close'."\r\n\r\n" 
   )) {
       exit('Failed adding request to output buffer\n');
   }
   
   if (!$bev->connectHost($dns_base, $argv[1], 80, EventUtil::AF_UNSPEC)) {
       exit('Can\'t connect to host '.$argv[1].PHP_EOL);
   }
   
   $base->dispatch();
   ?>

See also `Event <https://www.php.net/event>`_ and `libevent <http://libevent.org/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extevent                                                                                                                                                                     |
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


