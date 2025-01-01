.. _extensions-extpcntl:

.. _ext-pcntl:

ext/pcntl
+++++++++

.. meta::
	:description:
		ext/pcntl: Extension for process control.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/pcntl
	:twitter:description: ext/pcntl: Extension for process control
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/pcntl
	:og:type: article
	:og:description: Extension for process control
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extpcntl.html
	:og:locale: en
Extension for process control.

Process Control support in PHP implements the Unix style of process creation, program execution, signal handling and process termination. Process Control should not be enabled within a web server environment and unexpected results may happen if any Process Control functions are used within a web server environment.

.. code-block:: php
   
   <?php
   declare(ticks=1);
   
   $pid = pcntl_fork();
   if ($pid == -1) {
        die('could not fork'); 
   } else if ($pid) {
        exit(); // we are the parent 
   } else {
        // we are the child
   }
   
   // detatch from the controlling terminal
   if (posix_setsid() == -1) {
       die('could not detach from terminal');
   }
   
   // setup signal handlers
   pcntl_signal(SIGTERM, 'sig_handler');
   pcntl_signal(SIGHUP, 'sig_handler');
   
   // loop forever performing tasks
   while (1) {
   
       // do something interesting here
   
   }
   
   function sig_handler($signo) 
   {
   
        switch ($signo) {
            case SIGTERM:
                // handle shutdown tasks
                exit;
                break;
            case SIGHUP:
                // handle restart tasks
                break;
            default:
                // handle all other signals
        }
   
   }
   
   ?>

See also `Process Control <https://www.php.net/manual/en/book.pcntl.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extpcntl                                                                                                                                                                     |
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


