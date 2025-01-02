.. _extensions-extsem:

.. _ext-sem:

ext/sem
+++++++

.. meta::
	:description:
		ext/sem: Extension Semaphore, Shared Memory and IPC.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/sem
	:twitter:description: ext/sem: Extension Semaphore, Shared Memory and IPC
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/sem
	:og:type: article
	:og:description: Extension Semaphore, Shared Memory and IPC
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/sem.html
	:og:locale: en
Extension Semaphore, Shared Memory and IPC.

This module provides wrappers for the System V IPC family of functions. It includes semaphores, shared memory and inter-process messaging (IPC).

.. code-block:: php
   
   <?php
   
   $key         = ftok(__FILE__,'a');
   $semaphore   = sem_get($key);
   sem_acquire($semaphore);
   sem_release($semaphore);
   sem_remove($semaphore);
   
   ?>

See also `Semaphore, Shared Memory and IPC <https://www.php.net/manual/en/book.sem.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extsem                                                                                                                                                                       |
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


