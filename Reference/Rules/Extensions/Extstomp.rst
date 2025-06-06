.. _extensions-extstomp:


.. _stomp:

Stomp
+++++

.. meta::
	:description:
		Stomp: This extension allows php applications to communicate with any Stomp compliant Message Brokers through easy object-oriented and procedural interfaces.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Stomp
	:twitter:description: Stomp: This extension allows php applications to communicate with any Stomp compliant Message Brokers through easy object-oriented and procedural interfaces
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Stomp
	:og:type: article
	:og:description: This extension allows php applications to communicate with any Stomp compliant Message Brokers through easy object-oriented and procedural interfaces
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Stomp.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extstomp.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extstomp.html","name":"Stomp","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This extension allows php applications to communicate with any Stomp compliant Message Brokers through easy object-oriented and procedural interfaces","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Stomp.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This extension allows php applications to communicate with any Stomp compliant Message Brokers through easy object-oriented and procedural interfaces.

.. code-block:: php
   
   <?php
   
   $queue  = '/queue/foo';
   $msg    = 'bar';
   
   /* connection */
   try {
       $stomp = new Stomp('tcp://localhost:61613');
   } catch(StompException $e) {
       die('Connection failed: ' . $e->getMessage());
   }
   
   /* send a message to the queue 'foo' */
   $stomp->send($queue, $msg);
   
   /* subscribe to messages from the queue 'foo' */
   $stomp->subscribe($queue);
   
   /* read a frame */
   $frame = $stomp->readFrame();
   
   if ($frame->body === $msg) {
       var_dump($frame);
   
       /* acknowledge that the frame was received */
       $stomp->ack($frame);
   }
   
   /* close connection */
   unset($stomp);
   
   ?>

See also `Stomp <https://stomp.github.io/>`__.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extstomp                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


